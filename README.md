# Homekit Docker Standup

This is a docker-compose configuration to run home automation and bridge services on a Synology NAS, allowing you to connect non-HomeKit devices to Apple Home.

## 🚀 Services

| Service | Description |
| :--- | :--- |
| [Homebridge](https://homebridge.io/) | Connects non-HomeKit Smart Home devices to Apple HomeKit. |
| [Matterbridge](https://github.com/Luligu/matterbridge) | A bridge that exposes non-Matter devices to HomeKit via the Matter protocol. |
| [Scrypted](https://www.scrypted.app/) | High-performance video integration for cameras into HomeKit (HKSV). |

## 📋 Prerequisites

- Synology NAS (DSM 7.x recommended)
- [Git](https://git-scm.com/) installed via SynoCommunity
- [Docker / Container Manager](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## 🛠️ Setup

1. **Clone the project**:
   ```bash
   git clone https://github.com/phikai/homekit-docker-standup.git
   ```
2. **Environment Configuration**:
   - Copy `sample.env` to `.env`.
   - Update `SYNOLOGY_BASE_DOCKER_PATH` to your docker root (e.g., `/volume1/docker`).
   - Set your `PUID` and `PGID` (run `id` via SSH).
3. **Deploy**:
   ```bash
   docker compose up -d
   ```

## 🌐 Accessing Apps

> **Note**: These services run in `host` network mode for better device discovery.

| App | Default URL |
| :--- | :--- |
| **Homebridge** | `http://<NAS_IP>:${HOMEBRIDGE_UI_PORT}` |
| **Matterbridge** | `http://<NAS_IP>:8283` |
| **Scrypted** | `https://<NAS_IP>:10443` |

## ⚙️ Environment Variables

Common variables used across services:
- `PUID/PGID`: Local user/group IDs.
- `TZ`: Your timezone (e.g., `Europe/London`).
- `LOG_FILE_NUM/SIZE`: Settings for Docker log rotation.

---

If this project has helped you, please consider supporting my work!

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/G2G71SUNID)

---

# Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY.
