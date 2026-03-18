# Spotify Full-Stack App

A full-stack Spotify-style music app built with:

- **spotify-client**: User-facing React app
- **spotify-admin**: Admin dashboard to manage songs and albums
- **spotify-backend**: Express + MongoDB API with Cloudinary file uploads

## Project Structure

```text
spotify-full-stack/
  spotify-admin/
  spotify-backend/
  spotify-client/
```

## Tech Stack

- Frontend: React, Vite, Tailwind CSS
- Backend: Node.js, Express
- Database: MongoDB (Mongoose)
- Media Storage: Cloudinary

## Prerequisites

- Node.js 18+
- npm
- MongoDB connection URI
- Cloudinary account credentials

## Environment Variables (Backend)

Create a `.env` file in `spotify-backend/` with:

```env
PORT=4000
MONGODB_URI=your_mongodb_connection_string
CLOUDINARY_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_SECRET_KEY=your_cloudinary_secret_key
```

Notes:
- The backend connects to `${MONGODB_URI}/spotify`.
- Default server port is `4000`.

## Install Dependencies

Install dependencies in each app:

```bash
cd spotify-backend
npm install

cd ../spotify-client
npm install

cd ../spotify-admin
npm install
```

## Run the Project (Development)

Open 3 terminals and run each service separately.

### 1) Start Backend

```bash
cd spotify-backend
npm run server
```

Backend runs at `http://localhost:4000`.

### 2) Start Client App

```bash
cd spotify-client
npm run dev
```

### 3) Start Admin App

```bash
cd spotify-admin
npm run dev
```

## API Routes

Base URL: `http://localhost:4000`

### Song
- `POST /api/song/add`
- `GET /api/song/list`
- `POST /api/song/remove`

### Album
- `POST /api/album/add`
- `GET /api/album/list`
- `POST /api/album/remove`

## Important Notes

- Both frontend apps currently use hardcoded backend URL: `http://localhost:4000`.
- Ensure backend is running before opening client/admin apps.
- Uploaded media is stored in Cloudinary.

## Build for Production

### Client

```bash
cd spotify-client
npm run build
npm run preview
```

### Admin

```bash
cd spotify-admin
npm run build
npm run preview
```
