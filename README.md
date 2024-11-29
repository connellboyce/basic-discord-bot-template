# Basic Discord Bot Template

## How to run
Install dependencies with the following command:
```
pip install -r requirements.txt
```
Use the following command to run the bot:
```
python bot.py
```

## How to Use
#### Clone Template
- Create a new repository using this template.

#### Setup Bot in Discord Developer Portal
- Open the [Discord Developer Portal](https://discord.com/developers/applications)
- Click `New Application`
- Name it and agree to Terms & Conditions
  - Once created, you can customize as necessary
- Go to OAuth2 tab
  - Select scopes: `bot` and `messages.read`
  - Select permissions as needed. It is suggested to at minimum select the following:
    - General Permissions: `View Channels`
    - Text Permissions: `Send Messages`
  - Copy and paste the generated URL in your browser to invite the bot to one of your servers.
- Go to Bot tab
  - Enable `Message Content Intent`
  - Click `Reset Token`
    - Save this token for later, you will need to supply this as the `BOT_TOKEN` environment variable.

#### Update Contents
- This template is set up to return the response of an arbitrary API.
  - Update the logic as necessary to suit your needs.
- Alter the commands. The function name is what the bot uses as the command name. Update the default function name and create new command functions as needed.
- Update your `BOT_TOKEN` with the one obtained from the Discord Developer Portal.

#### Deploy
- This bot will need to be running 24/7. You can run it on your computer constantly, or you can deploy it.
  - If you try to host for free, you will need to ensure it has constant uptime, or else it will fail to listen properly.
- A service like [Render.com](https://www.render.com/) will allow you to host consistently for free.
- (Optional) Set up a pinging service, like [UptimeRobot](https://uptimerobot.com/) to ping your hosted application's Flask server (via keep_alive.py).
  - Many free services, such as Render will become idle if the application is not being accessed frequently enough, and so the above step may be needed.
 
#### Usage
- Once the bot is running, in a channel the bot has access to, enter the function name you'd like to execute, prepended by an exclamation point.
  - e.g.: `!command`
