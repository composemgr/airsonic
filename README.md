## 👋 Welcome to airsonic 🚀

Airsonic Advanced - Free web-based media streamer

## 📋 Description

Airsonic Advanced is a free, web-based media streamer providing ubiquitous access to your music. Stream to multiple players simultaneously, share with friends, or listen to your own music while at work. Based on Airsonic with advanced features and improvements.

## 🚀 Services

- **app**: Airsonic Advanced server (`lscr.io/linuxserver/airsonic-advanced:latest`)

## 📦 Installation

### Using curl
```shell
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/airsonic/main/docker-compose.yaml" | docker compose -f - up -d
```

### Using git
```shell
git clone "https://github.com/composemgr/airsonic" ~/.local/srv/docker/airsonic
cd ~/.local/srv/docker/airsonic
docker compose up -d
```

### Using composemgr
```shell
composemgr install airsonic
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York            # Timezone
SERVICE_USER=1000              # PUID for file permissions
SERVICE_GROUP=1000             # PGID for file permissions
CONTEXT_PATH=/                 # URL base path for reverse proxy
JAVA_OPTS=-Xms256m -Xmx512m   # Java memory settings
```

### Directory Structure

```
.
├── docker-compose.yaml
└── rootfs/
    ├── config/airsonic/       # Application config and database
    ├── data/
    │   ├── music/            # Your music library
    │   ├── playlists/        # Saved playlists
    │   └── podcasts/         # Podcast downloads
    └── db/sqlite/airsonic/   # SQLite database
```

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59037
- **Default Credentials**: admin / admin
- **Change password immediately after first login**

## 📂 Volumes

- `./rootfs/config/airsonic` - Configuration and transcoding cache
- `./rootfs/data/music` - Music library
- `./rootfs/data/playlists` - Playlists
- `./rootfs/data/podcasts` - Podcast storage

## 🔐 Security

- Change default admin/admin credentials immediately
- Configure user access and sharing permissions
- Use reverse proxy with HTTPS for external access
- Set appropriate file permissions (PUID/PGID)

## 🎵 Usage

1. First login with admin/admin
2. Change admin password in Settings → Users
3. Add media folders in Settings → Media folders
4. Scan library
5. Configure transcoding if needed
6. Start streaming!

## 🔍 Logging

```shell
docker compose logs -f app
```

## ��️ Management

```shell
# Start
docker compose up -d

# Stop
docker compose down

# Update
docker compose pull && docker compose up -d

# Rebuild library
# Go to Settings → Scan media folders now
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+
- Music files in supported formats (MP3, FLAC, OGG, etc.)
- FFmpeg (included in container) for transcoding

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
