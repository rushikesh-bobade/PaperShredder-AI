# AI-Hackfest-2k26

PaperShredder AI is a modern React Router web application that simulates AI-driven academic paper analysis with a polished, production-style user experience.

The product flow includes authentication, upload and processing simulation, contradiction analysis, rebuttal generation, audio narration UI, wallet and rate-limit views, and historical analysis tracking.

## Table of Contents

- Overview
- Tech Stack
- Product Features
- Project Structure
- Getting Started
- Available Scripts
- Build and Run
- Environment Variables
- Security Notes
- Development Workflow
- Deployment Notes
- Roadmap

## Overview

This repository powers a frontend-focused research review experience.

Current implementation focus:

- Clean, modular UI architecture
- Route-based page composition
- Context-driven state management
- Mock-backed analysis pipeline and rate-limit behavior
- SSR-capable build with React Router

## Tech Stack

- React 19
- React Router 7
- TypeScript 6
- Vite 7
- CSS Modules
- Lucide React icons

## Product Features

- Login flow with demo credentials
- Drag-and-drop PDF intake UI
- Multi-step analysis processing experience
- Analysis results dashboard including:
	- Summary card
	- Credibility score
	- Claims list
	- Contradiction matrix
	- Rebuttal card
	- Audio waveform player
	- Share/export actions
- History page with search, sorting, and pagination
- Wallet and usage/rate-limit dashboard
- Settings panels for voice, analysis preferences, APIs, and privacy actions

## Project Structure

High-level layout:

- app
	- blocks: reusable feature blocks grouped by page/domain
	- routes: route-level page components
	- hooks: state and utility hooks
	- data: mock domain models and sample datasets
	- styles: reset, global, and theme tokens
- public: static assets
- prompts: local prompt assets (ignored in Git)
- .agents: local assistant assets (ignored in Git)

## Getting Started

### Prerequisites

- Node.js 20 or newer
- npm 10 or newer

### Installation

```bash
npm install
```

### Start Development Server

```bash
npm run dev
```

Default local URL is shown in terminal output.

## Available Scripts

- npm run dev: Start development server
- npm run build: Create production build
- npm run start: Serve production build
- npm run typecheck: Generate route types and run TypeScript checks

## Build and Run

Build for production:

```bash
npm run build
```

Run production server:

```bash
npm run start
```

## Environment Variables

No required environment variables are needed for the current implementation.

The app is currently mock-backed and does not call external AI providers or blockchain services at runtime.

If you later integrate real services, add a local environment file and keep credentials out of client code.

## Security Notes

- This repository intentionally includes demo-only login values for local testing UX.
- Do not reuse demo credentials in real environments.
- Keep real API keys and private keys only in secure backend environments.
- Never embed secrets inside frontend source code.

## Development Workflow

Team branching standard for this repository:

- Create a new branch for each feature or bug fix
- Keep main as stable integration branch
- Push branches and open pull requests for review

Suggested branch naming:

- feature/short-description
- fix/short-description
- chore/short-description

## Deployment Notes

This app supports SSR-oriented build output via React Router build tooling.

Typical deployment flow:

1. npm ci
2. npm run typecheck
3. npm run build
4. npm run start (or platform equivalent process manager)

## Roadmap

Planned next-stage enhancements:

- Replace mock analysis with real service integrations
- Add persistent auth and session management
- Add backend API layer and secure credential handling
- Add automated test coverage (unit and integration)
- Add CI quality gates for linting, type checks, and build
