# chore: monorepo scaffolding with shared constants

## Summary

This PR sets up a clean monorepo structure containing contracts (Soroban), frontend (Next.js), and backend (Node.js), with shared constants/configuration at the root.

## Changes

- Initializes monorepo with npm workspaces
- Adds contracts (Soroban), frontend (Next.js), backend (Node.js)
- Introduces shared constants folder for network config
- Sets up root scripts and README

## Details

### 1. Root Project

- Created `package.json` with npm workspaces: `contracts`, `frontend`, `backend`, `constants`
- Added development scripts: `dev:frontend`, `dev:backend`, `build`, `install:all`

### 2. Folder Structure

```
stellar-polymarket/
├── contracts/       # Soroban smart contracts (Rust)
├── frontend/       # Next.js application
├── backend/        # Node.js API
├── constants/      # Shared configuration (@polymarket/constants)
└── package.json    # Root workspace config
```

### 3. Contracts (Soroban)

- Initialized Rust project with `cargo init`
- Located at `/contracts`

### 4. Frontend (Next.js)

- Placeholder created at `/frontend`
- Ready for `npx create-next-app@latest . --typescript`

### 5. Backend (Node.js)

- Created Express.js server at `backend/src/index.ts`
- Installed: express, dotenv, cors

### 6. Shared Constants

Created `@polymarket/constants` package with:

```typescript
export const NETWORK_PASSPHRASE = "Test SDF Network ; September 2015";
export const CONTRACT_IDS = { MARKET: "" };
export const HORIZON_URL = "https://horizon-testnet.stellar.org";
export const RPC_URL = "https://soroban-testnet.stellar.org";
```

### 7. Documentation

- Created README.md with setup instructions and architecture overview

## Validation

Run the following to validate:

```bash
npm install
npm run dev:frontend  # Next.js at http://localhost:3000
npm run dev:backend   # Node.js at http://localhost:3001
```

## Related Issues

Closes #1
