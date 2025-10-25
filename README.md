# Homekit Docker Standup

---
This is a simple docker-compose configuration to run some home automation apps on a Synology NAS.

## Services

- [Homebridge](https://homebridge.io/) - for connecting IOT Devices to Homekit
- [Matterbirdge](https://github.com/Luligu/matterbridge) - for connecting IOT Devices with Matter Support to Homekit
- [Scrypted](https://www.scrypted.app/) - for connecting Cameras to Homekit

## Install Instructions

### Prerequisites

- Synology NAS
- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/)
- [Docker-Compose](https://docs.docker.com/compose/)

### Setup

1. Clone this project
1. Copy `sample.env` to `.env` and update variables as appropriate
1. Run `docker-compose up -d` to start the services

## Accessing Apps

1. Homebridge will be available at the IP Address on the `HOMEBRIDGE_UI_PORT`, `http://192.168.x.x:58581`
1. Matterbridge will be available at the IP Adddress of your host on port `8283`, `http://192.168.x.x:8283`
1. Scrypted will be available at the IP Adddress of your host on port `10443`, `https://192.168.x.x:10443`

## Environment File

```plaintext
LOCALUSER=
PUID=
PGID=
LOG_FILE_NUM=5
LOG_FILE_SIZE=10m
TZ=
SYNOLOGY_BASE_DOCKER_PATH=/volume1/docker
HOMEBRIDGE_UI_PORT=
```

---

If this project has helped you in anyway, and you'd like to say thanks...

[![Donate](https://img.shields.io/badge/Donate-SquareCash-brightgreen.svg)](https://cash.me/$phikai)

---

# Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.