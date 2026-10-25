# YouTube Watch Party

A full-stack web application that allows multiple users to watch YouTube videos together in real time. Users can create or join rooms and synchronize video playback.

## Features

- Create and join watch-party rooms.
- Join using a room code or invitation link.
- Synchronize YouTube play, pause, seek, and video changes.
- Support Host, Moderator, and Participant roles.
- Allow the host to assign roles and remove participants.
- Real-time communication using WebSockets.

> Only claim features that are implemented and tested in your application.

## Technology Stack

- **Frontend:** React, Vite
- **Backend:** Node.js, Express
- **Real-time communication:** WebSockets or Socket.IO, depending on the implementation
- **Video integration:** YouTube IFrame Player API
- **Deployment:** Add your hosting platform after deployment

## Installation and Setup

### Prerequisites

- Node.js and npm
- Git
- Visual Studio Code or another code editor

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd web3task-watch-party
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

If the project provides an `.env.example` file, copy it to `.env` using PowerShell:

```powershell
Copy-Item .env.example .env
```

Configure any required environment variables according to the project setup.

### 4. Run the application

```bash
npm run dev
```

Open the frontend URL displayed in the terminal. In local development, it may be:

http://localhost:5173/

The backend may run at:

http://localhost:4000/

Use the actual ports and URLs configured in your project.

## Architecture Overview

The frontend provides the user interface, watch-party rooms, participant list, and YouTube player.

The Node.js and Express backend handles API requests and room-related logic. WebSocket communication allows the server and connected clients to exchange real-time events.

When an authorized user changes playback, the backend validates the action and broadcasts the updated state to other participants in the same room. Their clients then update their video players.

## Role-Based Access Control

- **Host:** Controls playback, assigns roles, and removes participants.
- **Moderator:** Controls playback according to the permissions implemented.
- **Participant:** Watches the video without direct playback control.

The backend should validate permissions before processing restricted actions.

## Project Links

- **GitHub Repository:** YOUR_GITHUB_REPOSITORY_URL
- **Live Application:** ADD_YOUR_DEPLOYED_FRONTEND_URL
- **Backend URL:** ADD_YOUR_DEPLOYED_BACKEND_URL

## Testing Checklist

- [ ] Create a watch-party room.
- [ ] Join the room from another browser.
- [ ] Test play and pause synchronization.
- [ ] Test seek synchronization.
- [ ] Test changing the YouTube video.
- [ ] Test host and moderator permissions.
- [ ] Test participant promotion and removal.
- [ ] Verify the deployed application works.

## Author

Your Name

YouTube Watch Party — Full Stack Internship Assignment
