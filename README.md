# Zurich Transport Display

A minimalistic web application displaying real-time public transport departures for Zurich, designed for Raspberry Pi wall displays.

## Features

- Real-time departures for buses, trams, and trains
- Smart autocomplete with offline fallback
- Zurich city official design style
- Auto-refresh every minute
- Responsive design for small screens
- Docker containerized for easy deployment

## Quick Start

### Docker Run

```bash
docker run -d -p 8080:80 --name zurich-transport your-username/zurich-transport
```

### Docker Compose

```bash
docker-compose up -d
```

### Portainer Deployment

1. Go to Portainer → Stacks
1. Click “Add stack”
1. Name: `zurich-transport`
1. Paste the docker-compose.yml content
1. Deploy

## Configuration

The app includes common Zurich stations for offline functionality:

- Zurich HB, Bellevue, Paradeplatz
- Oerlikon, Stadelhofen, Hardbrücke
- And many more…

## API

Uses the official Swiss public transport API: `transport.opendata.ch`

## Development

### Local Development

```bash
# Clone the repository
git clone https://github.com/your-username/zurich-transport-display.git
cd zurich-transport-display

# Build and run
docker build -t zurich-transport .
docker run -p 8080:80 zurich-transport
```

### File Structure

```
.
├── index.html          # Main application
├── Dockerfile          # Docker configuration
├── docker-compose.yml  # Docker Compose setup
├── nginx.conf          # Nginx configuration
└── README.md          # This file
```

## Raspberry Pi Setup

1. Install Docker on your Raspberry Pi
1. Clone this repository
1. Run with docker-compose
1. Set browser to fullscreen mode for wall display
1. Optionally set up auto-refresh with cron

## Environment Variables

- `TZ`: Timezone (default: Europe/Zurich)

## Health Check

Health endpoint available at `/health` for monitoring.

## License

MIT License

## Contributing

1. Fork the repository
1. Create a feature branch
1. Commit your changes
1. Push to the branch
1. Create a Pull Request
2. 
