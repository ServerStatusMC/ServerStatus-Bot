# Server Status - Discord Bot
**A real time server status plugin**

*Note: this bot is still a WIP and very subject to change*

The Discord runs on a Discord server changing the names and descriptions of channels as people leave and join the server. The bot can change the titles of 2 voice channels, it's recommended that these are restricted for best use, to display the current status of the server and player count. The bot also dynamically changes the descriptions of any provided text channels to display the status and player count, in addition to listing players online.

## Installation
The install for the Discord bot is similar to the webserver. Once you have it downloaded, run `npm install` in the direcotry to install the dependencies, and `npm start` to start it! To get it onto your server you can use [this guide](https://www.howtogeek.com/364225/how-to-make-your-own-discord-bot/) from How To Geek.

## Configuration
The `web_socket` section of this configuration is similar to the plugin. Enter in the address and port of your webserver to get Socket.io to connect. The rest of the bot's setup is found in the `discord` section. In `channels` you can add the ids of the channels you want the bot to modify (*make sure you keep the id's in quotes*). If you don't know how to get channel id's you can follow [this guide](https://www.youtube.com/watch?v=NLWtSHWKbAI) by Gauging Gadgets. Next, like the website, set the max players of your server in `max_players` as the plugin doesn't query that information. Here you can also set the status you want your bot to have and the type. The available types are `PLAYING` (Playing), `WATCHING` (Watching), and `LISTENING` (Listening to). Finally, enter the token you got from the Discord developer dashboard into the `token` area, save, and restart the bot.

### Default configuration:
```
# Configuration for the websocket used to contact the server
web_socket:
  # Web server address
  address: 'http://localhost'
  # Web server port
  port: 80

# Discord bot settings
discord:
  
  # Channel id setup
  # Make sure to use quotes!
  channels:
    # Online/Offline status voice channel
    voice_status: ''
    # Player count voice channel
    voice_players: ''
    # Player count text channels
    text:
      - ''
  
  # Minecraft Server max players
  max_players: 20
  
  # Discord status
  status:
    # Status type
    # Options: PLAYING, WATCHING, LISTENING
    type: 'WATCHING'
    # Status message
    message: 'My Minecraft Server'
  
  # Discord bot token
  token: 'TOKEN'
```
