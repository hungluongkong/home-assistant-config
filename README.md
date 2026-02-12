# 🏠 Home Assistant Config

Personal Home Assistant setup, managed via Docker.

## Quick Start

### Prerequisites
- Docker & Docker Compose
- Windows / Linux / macOS

### Run

```bash
docker compose up -d
```

Home Assistant will be available at: **http://localhost:8123**

### First Setup
1. Open `http://localhost:8123` in browser
2. Create your admin account
3. Follow the onboarding wizard
4. Add devices via **Settings → Devices & Services → Add Integration**

## Supported Integrations

Ready to add:
- 💡 **Tuya / Smart Life** - Smart plugs, lights, switches
- 🌡️ **Xiaomi Mi** - Temperature/humidity sensors
- 📹 **ONVIF** - IP cameras
- 🔌 **MQTT** - Custom IoT devices
- 📱 **Mobile App** - Phone as a sensor/controller

## OpenClaw Integration

This setup includes the REST API enabled. To connect OpenClaw:

1. Generate a **Long-Lived Access Token** in HA:
   - Profile → Security → Long-Lived Access Tokens → Create Token
2. Use the token to call HA APIs:
   ```bash
   curl -H "Authorization: Bearer YOUR_TOKEN" http://localhost:8123/api/states
   ```

## File Structure

```
├── docker-compose.yml      # Docker setup
├── config/
│   ├── configuration.yaml  # Main config
│   ├── automations.yaml    # Automation rules
│   ├── scripts.yaml        # Scripts
│   ├── scenes.yaml         # Scenes
│   └── secrets.yaml        # Secrets (not committed)
└── README.md
```

## Timezone

Configured for **Asia/Ho_Chi_Minh (UTC+7)**
