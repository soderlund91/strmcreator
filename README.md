STRM Creator is a high-performance tool designed to transform IPTV playlists (M3U) into .strm files. This allows you to integrate your IPTV provider's content directly into media libraries like Plex, Jellyfin, or Emby as if they were local files.

Made with a lot of helt from ChatGPT and Google Gemini.

Key Features

🚀 High Performance: Parallel processing engine capable of handling thousands of streams in seconds.

💎 4K/UHD Separation: Automatically detects quality tags and organizes content to prevent 4K files from overwriting HD versions.

📂 Smart Organization: Automatically maps series into proper Season folders that media servers love.

🧹 Name Normalization: Built-in cleaning of unnecessary tags (e.g., language codes, codecs, and release info) for a clean library look.

🌐 Web UI: User-friendly interface to trigger runs and monitor logs in real-time.

🛠 Installation (Docker Compose)
Running STRM Creator via Docker Compose is the recommended method.

1. Create a folder for the project.

2. Create a file named docker-compose.yml and paste the following:

```
services:
  strmcreator:
    image: soderlund91/strmcreator:latest
    container_name: strmcreator
    restart: unless-stopped
    ports:
      - "8585:8000"
    volumes:
      - ./config:/config
      - ./data:/data
      - ./media:/media  # Change to where you want your media (left side of the : )
    environment:
      - TZ=UTC
```
3. Start the container:

```
docker-compose up -d
```
4. Go to
```
http://localhos:8585/ui
```
5. Enter your URL for your m3u file and hit save.
6. Update groups and mark what you whant. (This code is only tested with movies and series, not live channels)
7. Hit "Run now"
