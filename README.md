# Aʟᴇxᴀ
![Alexa](https://telegra.ph/file/a5ec644be1e5ff9ac991c.jpg)
A Telegram Group MANAGER Bot It Can Easily Manage Your Group!!!!!
## Aʙᴏᴜᴛ Aʟᴇxᴀ 
A Telegram Pro Group MANAGER Bot. Made by [Duvvado jagannadham](https://t.me/Beast_boy_shubu) . This Bot has AI feature (It can Talk Like Humans) Group manager bot.

### Fᴏʀᴋ ᴀᴛ ʏᴏᴜʀ ᴏᴡɴ ʀɪsᴋ


# Hᴏᴡ ᴛᴏ sᴇᴛᴜᴘ/ᴅᴇᴘʟᴏʏ.

## Read these notes carefully before proceeding 
 - Edit any mentions of @Alexasupportchannel to your own support chat. 
 - Your code must be open source and a link to your fork's repository must be there in the start reply of the bot. [See this](https://github.com/AnimeKaizoku/SaitamaRobot/blob/shiken/SaitamaRobot/__main__.py#L25)
 - Lastly, if you are found to run this repo without the code being open sourced or the repository link not mentioned in the bot, we will push a gban for you in our network because of being in violation of the license, you are free to be a dick and not respect the open source code (we do not mind) but we will not be having you around our chats.

# Dᴇᴘʟᴏʏ ᴛᴏ ʜᴇʀᴏᴋᴜ
Click below icon to create own Alexa Bot.
 
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Starting the bot.

Once you've setup your database and your configuration (see below) is complete.


## Setting up the bot (Read this before trying to use!):
Please make sure to use Docter, as I cannot guarantee everything will work as expected on older python versions!
This is because markdown parsing is done by iterating through a dict, which are ordered by default in 3.6.

### Configuration

There are two possible ways of configuring your bot: a config.py file, or ENV variables.

The prefered version is to use a `config.py` file, as it makes it easier to see all your settings grouped together.
This file should be placed in your `tg_bot` folder, alongside the `__main__.py` file . 
This is where your bot token will be loaded from, as well as your database URI (if you're using a database), and most of 
your other settings.

It is recommended to import sample_config and extend the Config class, as this will ensure your config contains all 
defaults set in the sample_config, hence making it easier to upgrade.

An example `config.py` file could be:
```
from tg_bot.sample_config import Config


class Development(Config):
    OWNER_ID = 570400686  # my telegram ID
    OWNER_USERNAME = "peroboy"  # my telegram username
    API_KEY = "your bot api key"  # my api key, as provided by the botfather
    SQLALCHEMY_DATABASE_URI = 'postgresql://username:password@localhost:5432/database'  # sample db credentials
    MESSAGE_DUMP = '-1234567890' # some group chat that your bot is a member of
    USE_MESSAGE_DUMP = True
    SUDO_USERS = [18673980, 83489514]  # List of id's for users which have sudo access to the bot.
    LOAD = []
    NO_LOAD = ['translation']
```

If you can't have a config.py file (EG on heroku), it is also possible to use environment variables.
The following env variables are supported:
