## 👋 Welcome to airsonic 🚀

Self-hosted airsonic application

## 📋 Description

Self-hosted airsonic application

## 🚀 Services

- **server**: lscr.io/linuxserver/airsonic-advanced:latest

## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/airsonic/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/airsonic" ~/.local/srv/docker/airsonic
cd ~/.local/srv/docker/airsonic
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install airsonic
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
SERVICE_USER=0
SERVICE_GROUP=0
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59089

## 📂 Volumes

- `./volumes/data/media/music` - Data storage
- `./volumes/data/media/podcasts` - Data storage
- `./volumes/data/media/playlists` - Data storage
- `./volumes/data/airsonic` - Data storage

## 🔍 Logging

```shell
docker compose logs -f server
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
