# GDU Bot

A feature-rich Discord bot built with TypeScript, Discord.js, and TypeORM.

## Overview

GDU Bot is a comprehensive Discord bot featuring multiple plugins including dailies tracking, utilities, moderation, fun commands, and more. The bot is designed with a modular plugin system, allowing for easy extensibility and maintenance.

## Features

### Core Plugins

- **Dailies** - Track daily streaks and challenges with alerts and mercy tracking
- **Fun** - Entertainment commands including 8Ball
- **GDU Utilities** - Server-specific utilities and event management
- **Info** - Bot information, help, stats, and server details
- **Manage** - Custom commands, prefixes, and server management
- **Markdown** - Text formatting utilities for channels, emojis, roles, and users
- **Moderation** - Message and member moderation with audit log tracking
- **Utilities** - Advanced utilities including code evaluation, URL shortening, and rendering

### Key Technologies

- **Discord.js** v13.6.0 - Discord API wrapper
- **TypeORM** - Object-relational mapping with SQLite database
- **Framed.js** - Discord bot framework
- **TypeScript** - Type-safe development
- **Koa** - Web framework for API routes
- **Winston** - Logging framework

## Requirements

- Node.js >= 16.0.0
- npm or pnpm

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Yupsecous/gdu-bot.git
cd gdu-bot
```

2. Install dependencies:
```bash
pnpm install
# or
npm install
```

3. Configure environment variables:
```bash
cp example.env .env
```

4. Update `.env` with your configuration:
```env
DISCORD_TOKEN="Your Discord Bot Token"
TYPEORM_WINSTON_LOGGER_LEVEL="db_silly"
LOGGER_LEVEL="silly"
API_PORT=42069
DEFAULT_PREFIX="."
SUGGEST_CHANNEL_ID=your_channel_id
```

## Development

### Build the project:
```bash
pnpm build
```

### Watch mode (with automatic rebuild):
```bash
pnpm build:watch
```

### Start the bot:
```bash
pnpm start
```

### Development with hot-reload:
```bash
pnpm dev
```

### Database Management:
```bash
pnpm typeorm
```

## Project Structure

```
src/
├── database/
│   ├── entities/          # TypeORM database entities
│   ├── interfaces/        # Database-related interfaces
│   └── types/             # Database type definitions
├── logger/                # Logging utilities
├── managers/              # Business logic managers
├── plugins/               # Plugin implementations
│   ├── Dailies/
│   ├── Fun/
│   ├── GDUUtilities/
│   ├── Info/
│   ├── Manage/
│   ├── Markdown/
│   ├── Moderation/
│   └── Utilities/
├── providers/             # TypeORM data providers
└── structures/            # Core bot structures
```

## Commands & Prefix

The default prefix is `.` but can be customized per server using the `prefix` command in the Manage plugin.

### Command Categories

- **Info** - `about`, `ping`, `help`, `server`, `botstat`, etc.
- **Dailies** - `dailies`, `streak`, `alert`, `vacation`, etc.
- **Moderation** - `clear`, moderation events
- **Utilities** - `eval`, `link`, `render`, `avatar`, etc.
- **Fun** - `8ball`
- **Manage** - `prefix`, custom commands, groups

## Docker

### Running with Docker Compose:
```bash
docker-compose up
```

### Development with Docker:
```bash
docker-compose -f debug-compose.yml up
```

## Contributing

Contributions are welcome! Please ensure:
- Code follows TypeScript best practices
- Changes maintain type safety
- Database migrations are properly handled

## License

MIT - See LICENSE file for details

## Author

Created by some1chan, maintained by Yupsecous

## Support

For issues and feature requests, please visit: https://github.com/Yupsecous/gdu-bot/issues

## Version

Current version: 0.10.1
