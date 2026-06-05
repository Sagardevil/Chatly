# Chatting application

## Project Overview

- **Name**: Chatting application
- **Description**: Real-time chat app with a Node.js/Express backend and a Vite + React frontend. Features user authentication, conversations, real-time messaging using Socket.IO, and media uploads via Cloudinary.

## Features

- **Real-time messaging**: Socket.IO-based messaging with conversation threads.
- **Authentication**: JWT-based auth and protected routes.
- **Media uploads**: Images/files stored via Cloudinary.
- **State management**: Redux slices for auth, conversations, messages, socket.
- **REST API**: Endpoints for users, messages, and conversations.
- **Audio & Video calls**: Peer-to-peer audio and video calling using WebRTC with signaling handled by Socket.IO. Supports one-to-one and group calls.
- **Screen sharing**: Share screen during calls for collaboration and demonstrations.

## Repository layout

- `backend` — Express server, controllers, models, socket logic.
- `frontend` — Vite + React app, components, Redux store.

## Prerequisites

- Node.js v16+ (recommended)
- npm or yarn
- MongoDB (local or hosted)
- Cloudinary account (for uploads)

## Environment variables (backend)

Create a `.env` file in `backend/` with at least:

- `MONGODB_URI` — MongoDB connection string
- `JWT_SECRET` — JWT signing secret
- `PORT` — Backend port (e.g., 5000)
- `CLOUDINARY_NAME` — Cloudinary cloud name
- `CLOUDINARY_API_KEY` — Cloudinary API key
- `CLOUDINARY_API_SECRET` — Cloudinary API secret

## Local setup

1. Install dependencies

```bash
# backend
cd backend
npm install

# frontend
cd ../frontend
npm install
```

2. Run in development

```bash
# start backend
cd backend
npm run dev

# start frontend
cd ../frontend
npm run dev
```

Replace `npm run dev` with the appropriate `start` script if your `package.json` differs.

## Testing

If tests exist, run them from the relevant folder:

```bash
cd backend
npm test

cd ../frontend
npm test
```

## Deployment

Common deployment flow:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```

- Host the backend on Heroku / Railway / Render / Azure / etc.
- Host the frontend on Vercel / Netlify / static hosting and configure it to use the deployed backend URL.

## Security & Notes

- Never commit `.env` files or secrets. Keep `JWT_SECRET` and Cloudinary credentials private.
- Add `backend/node_modules`, `frontend/node_modules`, and any `.env` files to `.gitignore`.

## Contributing

- Open issues and PRs. Follow existing code style and add tests for new logic.

## License

Choose and add a license (for example, MIT).

## Contact

- Add maintainer contact info or GitHub profile.
