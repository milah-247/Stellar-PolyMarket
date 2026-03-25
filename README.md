# Stellar PolyMarket

Monorepo for Stellar PolyMarket - Soroban smart contracts, Next.js frontend, Node.js backend

## Folder Structure

```
stellar-polymarket/
├── contracts/       # Soroban smart contracts
├── frontend/       # Next.js application
├── backend/        # Node.js API
├── constants/      # Shared configuration
└── package.json    # Root workspace config
```

## Prerequisites

- Node.js 18+
- Rust (for Soroban contracts)
- npm or yarn

## Setup

```bash
# Install all workspace dependencies
npm install

# Or using the script
npm run install:all
```

## Development

### Frontend

```bash
npm run dev:frontend
```

Runs the Next.js frontend at http://localhost:3000

### Backend

```bash
npm run dev:backend
```

Runs the Node.js API at http://localhost:3001

## Build

```bash
npm run build
```

Builds all workspaces.

## Shared Constants

The `constants` package contains shared network configuration:

- `NETWORK_PASSPHRASE` - Stellar network passphrase
- `CONTRACT_IDS` - Contract addresses
- `HORIZON_URL` - Horizon API URL
- `RPC_URL` - Soroban RPC URL

## Architecture

- **contracts/**: Soroban smart contracts written in Rust
- **frontend/**: Next.js 14+ with TypeScript
- **backend/**: Express.js API server
- **constants/**: Shared TypeScript configuration package
