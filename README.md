# Spotify Clone
We made a spotify clone for our college minor project

## Features

- Offline Streaming
- 🔗 **Collaboration:** users can join each others stream via a link.
- 🎵 **User Authentication**: Sign up, log in, and manage user sessions.
- 🎶 **Music Streaming**: Play, pause, and skip songs seamlessly.
- 📂 **Playlist Management**: Create, edit, and delete playlists.
- 🔍 **Search Functionality**: Find songs, albums, and artists.
- ❤️ **Like & Save**: Mark favorite tracks and add them to the library.
- ⏯ **Playback Controls**: Volume control, shuffle, and repeat modes.
- 🌙 **Dark Mode**: Toggle between light and dark themes.
- 📊 **Real-time Analytics**: Track user engagement with music plays.
- 🖼️ Spotify-Like player with GIF as player background.

## Problems

- Cloudinary does not support segmentation/chunkification
- Other databases are not that good when it comes to content optimization and delivery
- MongoDB can't store objects

## Data Models

### **User**

```json
{
  "id": "uuid",
  "name": "string",
  "email": "string",
  "password": "hashed string",
  "created_at": "timestamp"
}
```

### **Song**

```json
{
  "id": "uuid",
  "title": "string",
  "artist_id": "uuid",
  "album_id": "uuid",
  "duration": "integer (seconds)",
  "url": "string (audio file URL)",
  "created_at": "timestamp"
}
```

### **Playlist**

```json
{
  "id": "uuid",
  "name": "string",
  "user_id": "uuid",
  "songs": ["song_id1", "song_id2", ...],
  "created_at": "timestamp"
}
```

## Tech Stack

- **Frontend:** React.js
- **Backend:** Node.js, Express.js
- **Database:** PostgreSQL, MongoDB
- **Authentication:** Supabase Auth, JWT
- **Storage:** Cloudinary, AWS S3
- **Streaming:** WebRTC, HLS
- **Deployment:** Vercel

