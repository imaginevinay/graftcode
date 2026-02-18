# Graftcode

A simple full-stack project demonstrating how to package backend functions using **Graftcode** and consume them in a frontend application.

---

## Project Structure

```
graftcode/
├── backend/
└── frontend/
```

- **backend/** – Contains backend functions to be packaged and published.
- **frontend/** – Frontend application that consumes the packaged backend service.

---

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd graftcode
```

---

## Backend Setup

1. Navigate to the backend directory:

```bash
cd backend
```

2. Package and upload backend functions to the Graftcode private repository:

```bash
sudo gg --projectKey <project_key> --modules ./backend
```

3. After successful execution:

- Backend functions will be published as a package.
- Logs will display:
  - A locally hosted `gg` server
  - An `npm install` command with a generated registry token

> Save the generated registry URL and token from the logs. You will need it for frontend setup.

---

## Frontend Setup

1. Navigate to the frontend directory:

```bash
cd ../frontend
```

2. Install the backend package using the registry URL from the backend logs:

```bash
npm install --registry https://grft.dev/<token_generated_from_logs>__graftcode @graft/npm-service-backend@1.0.0
```

3. Start the development server:

```bash
npm run dev
```

4. Open your browser:

```
http://localhost:3000
```

---

## Expected Output

- The frontend runs on `http://localhost:3000`
- The backend service response is displayed in the UI

---

## Requirements

- Node.js (v18+ recommended)
- npm
- Graftcode CLI (`gg` command)

---

## Troubleshooting

- Ensure `<project_key>` is correct.
- Verify the registry token from logs is copied accurately.
- Confirm the package version matches the published version.
