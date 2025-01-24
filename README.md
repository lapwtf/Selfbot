# Server Protection Module

The Server Protection module is a comprehensive Discord bot security system designed to protect servers from unauthorized administrative actions, raids, and potential abuse. This module provides various security features and commands to help server owners maintain control and safety of their Discord servers.

## ⚠️ IMPORTANT WARNING

**USER ACCOUNT AUTOMATION IS AGAINST DISCORD'S TERMS OF SERVICE**

Using this or any other automation with user accounts (self-bots) is:
- Strictly forbidden by Discord's Terms of Service
- Can result in permanent account termination
- May lead to legal action from Discord
- Could result in your server being deleted

## Features

### Core Protection Features
- **Raid Detection**: Monitors and prevents unauthorized:
  - Channel creation/deletion
  - Role creation/deletion
  - Server setting modifications
  - Mass bans/kicks
  - Mass mentions
  - @everyone/@here abuse

### Punishment System
Configurable punishment types:
- Ban
- Kick
- Timeout
- Role Strip
- None (logging only)

### Whitelist System
- Maintains a list of trusted users exempt from protection measures
- Persistent storage using JSON files
- Commands to add/remove users from whitelist

### Logging System
- Configurable logging channel
- Detailed audit logs for all protection events
- Timestamps and user tracking

## Commands

### Configuration Commands
- `detection [on/off]` - Toggle raid detection
- `setpunishment [type]` - Set punishment type
- `setlog [channel]` - Set logging channel
- `autoslow [seconds]` - Configure auto slowmode
- `noinvite` - Toggle invite blocking

### User Management Commands
- `swhitelist [user]` - Add user to whitelist
- `sunwhitelist [user]` - Remove user from whitelist
- `banlist` - View all banned users
- `stripall` - Remove admin roles from non-whitelisted users

### Ban Management Commands
- `softban [user] [reason]` - Ban and immediately unban user
- `hardban [user] [reason]` - Permanently ban user
- `unhardban [user]` - Remove user from hardban list
- `ghostban [user_id] [reason]` - Ban user by ID
- `multiban [user_ids]` - Ban multiple users at once

## Setup

1. Add the module to your bot's cogs
2. Set up a logging channel using `setlog`
3. Configure desired punishment type using `setpunishment`
4. Add trusted staff to whitelist using `swhitelist`
5. Enable detection using `detection on`

## Security Notes

- All commands require owner permissions
- Whitelisted users bypass all protection measures
- Actions are logged for accountability
- Protection measures are reversible
- Hardban list persists across bot restarts

## Files
- `whitelist.json` - Stores whitelisted user IDs
- `protection_settings.json` - Stores module configuration

## Dependencies
- discord.py
- aiohttp
- typing
- json
- asyncio
- datetime

## Best Practices
1. Always maintain an up-to-date whitelist
2. Regularly review logs for suspicious activity
3. Test protection features in a development server first
4. Keep backup of configuration files
5. Regularly update trusted staff list

## Support
Just make an issue tbh. 
