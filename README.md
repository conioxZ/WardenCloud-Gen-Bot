# Discord Stock Generator Bot

A clean, production-ready Discord.js v14 bot for generating private inventory items from text-based stock files.

## Overview

This bot lets you manage inventory categories from simple `.txt` files in the `stock` folder. Each file becomes a category, and each line inside the file is treated as one available item.

## Features

- Slash commands: `/help`, `/stock`, `/gen`
- Prefix commands: `!help`, `!stock`, `!gen`
- Dynamic inventory detection from the `stock` folder
- Autocomplete for `/gen`
- Channel restriction for generation commands
- DM delivery for generated items
- Lightweight Express health endpoint
- Simple configuration through `config.js` and `.env`

## Project Structure

- `index.js` - Main bot logic
- `config.js` - Bot settings and environment-backed configuration
- `.env` - Secret environment variables
- `.env.example` - Sample environment file
- `stock/` - Inventory files (`.txt`)
- `README.md` - Project documentation
- `LICENSE` - MIT license

## Installation

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create your environment file:
   ```bash
   copy .env.example .env
   ```

3. Fill in your values in `.env`:
   - `TOKEN`
   - `CLIENT_ID`
   - `GUILD_ID`
   - `GEN_CHANNEL_ID`

## Running

Start the bot with:

```bash
npm start
```

## Inventory Format

Any `.txt` file inside the `stock` folder becomes an inventory category automatically.

Example:
- `stock/keys.txt`
- `stock/licenses.txt`
- `stock/giftcodes.txt`

Each line in a file represents one inventory item.

## Notes

- New `.txt` files are detected automatically while the bot is running.
- Generation commands only work in the configured channel from `GEN_CHANNEL_ID`.

## License

Made by UnknownzOp.

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
