# DiscordEcho: Announcement Maestro
***
<p align="center">
   <img src="https://readme-spotify-status-rho.vercel.app/api/run-spotify-status.py" alt="s4nx Playing Now" width="500" />
<p align="center">

# Overview 🌟

- **Red is a fully modular bot**, allowing you to toggle features and commands on/off according to your preferences, ensuring complete customization. It's a self-hosted bot, necessitating you to host and maintain your instance. Red can serve as an admin bot, music bot, trivia bot, your new best friend, or any combination thereof.

## Getting Started 🚀

1. Install Yarn if not already done: `npm i -g yarn` or `sudo npm i -g yarn` (for Unix systems).
2. Fork/Clone the repository.
3. Install dependencies by typing `yarn`.
4. Duplicate `.env.example` as a new file named `.env`.
5. Execute `yarn build` to construct the Prisma schema.
6. Create a volume for the Postgres database using `docker volume create --name=postgres`.
7. Initiate the database with `docker-compose up --build postgres`, which exclusively launches the Postgres container.
8. Update the `DATABASE_URL` environment variable in `/apps/bot` with `postgresql://postgres:internalpassword@localhost:5432/bot?schema=public`.
9. Before testing, ensure to push the schema to the database using `yarn pushdb` (this must be rerun every time changes are made to `prisma/schema.prisma`).
10. Test by executing `yarn dev`. Each time you save a file, the running instance will automatically halt, rebuild, and restart.

## Installation Made Easy 🛠️

Installation is straightforward, and you do not require any coding knowledge! Beyond installation and updates, every aspect of the bot can be managed directly within Discord.

## Default Modules 📦

The default set of modules includes, but is not limited to:

- Moderation features (kick, ban, softban, hackban, mod-log, filter, chat cleanup)
- Trivia (predefined lists and easy addition of new ones)
- Music features (YouTube, SoundCloud, local files, playlists, queues)
- Stream alerts (Twitch, Youtube, Picarto)
- Bank (slot machine, user credits)
- Custom commands
- Imgur/GIF search
- Admin automation (self-role assignment, cross-server announcements, mod-mail reports)
- Customizable command permissions

Furthermore, you can effortlessly discover and integrate other [Plugins](#plugins) (cogs) from our thriving community of cog repositories.

# Installation Guides 📄

We officially support the following platforms:

- [Windows](https://docs.discord.red/en/stable/install_guides/windows.html)
- [MacOS](https://docs.discord.red/en/stable/install_guides/mac.html)
- [Most major Linux distributions](https://docs.discord.red/en/stable/install_guides/index.html)

If you encounter issues after consulting the guide, don't hesitate to join the and seek assistance in the Discord channel.
<h3 align="left">
  <a href="https://discord.gg/hashnode"><img src="https://user-images.githubusercontent.com/35542790/210373056-35ba21a9-79b4-4bc1-a06a-0153dc14d97d.png" width="150" alt="Official Discord Server"></a>
</h3>

# Plugins 🧩

Red boasts full modularity, enabling you to load, unload, and directly install 3rd party plugins from Discord. A few examples include:

- Cleverbot integration (interact with Red and she'll respond)
- Ban synchronization
- Welcome messages
- Casino
- Reaction roles
- Slow Mode
- AniList integration
- And much more!

Feel free to explore the list of available 3rd party cogs [HERE](https://index.discord.hashnode)!

# Join the Community! 🌟

**DiscordEcho** is constantly evolving and is supported by an engaged community that contributes fresh content (cogs/plugins) for everyone's enjoyment. New features are regularly integrated. If you can't [LOCATE](https://index.discord.red) the cog you're looking for, check out our [GUIDE](https://docs.discord.red/en/stable/guide_cog_creation.html) on creating your own cogs!

- **Here are some examples of cogs:**

🔍 **BavarianVerifier**
- Verifies whether the author of a group-pinged message is part of that group and enforces a timeout if not. Includes a flair message for group members.

🐌 **CheckSnail**
- Maintains a list of the unique IDs of the last 1000 tweets in channels and notifies users of reposts.

🎬 **Cinephile**
- Uses regex to extract movie titles in the <TITLE> (<release year>) format and pairs them with newspaper NLP methods to generate a Letterboxd review of the movie.

📚 **Scholar**
- Extracts authors and publication year from a paper mentioned in the message, then crawls Google Scholar to retrieve the title and abstract of the paper.

📖 **WikiCrawl**
- Utilizes a Wikipedia API to fetch summaries of Wikipedia articles related to a given term.

# License 📜

This project is released under the [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.en.html) license.

The name "Red" is inspired by the main character of the video game "Transistor," developed by [Super Giant Games](https://www.supergiantgames.com/games/transistor/).

Artwork for the Red Discord Bot Project was created by [Sinlaire](https://sinlaire.deviantart.com/) on DeviantArt.

This project includes the [discord.ext.menus](https://github.com/Rapptz/discord-ext-menus) package developed by Danny Y. (Rapptz), distributed under the MIT License. A copy of this license is available in the [discord-ext-menus.LICENSE](redbot/vendored/discord-ext-menus.LICENSE) file in the [redbot/vendored](redbot/vendored) folder of this repository.
