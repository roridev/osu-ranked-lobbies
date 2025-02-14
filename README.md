# osu! ranked lobbies

A bot that creates osu! lobbies, with an alternative leaderboard not based on performance points.

Contributions are welcome; if you have trouble getting the bot to run, feel free to message kiwec on discord (or on osu!).

### Development setup

* `yarn install`

* Copy `config.json.example` to `config.json` and add the required API keys.

The `sentry_dsn` setting is only required if you intend to run the bot in production, as it is used for error monitoring.

* Download `maps.db` [from my website](https://osu.kiwec.net/maps.db)

You can also build it yourself, but the scripts required to do so no longer exist (lol) and it takes a long time.

* Download and extract the latest `osu_files.tar.bz2` file [from data.ppy.sh](https://data.ppy.sh/) and extract the `.osu` files to the `maps/` directory

This step isn't required, but makes profile scanning faster and avoids spamming the osu! servers with requests.

### Feature flags

During development, you might not want to run the entire bot. You can disable the following feature flags in config.json:

* `CONNECT_TO_BANCHO`: connects to the osu! servers, rejoins lobbies, replies to in-game commands, etc.

* `CREATE_LOBBIES`: creates 4 lobbies automatically. Highly recommended to disable this (or edit the lobby creation code in index.js) during development.

* `CONNECT_TO_DISCORD`: connects to the discord api, reacts to interactions, changes user roles, etc.

* `HOST_WEBSITE`: hosts the o!rl website on port 3001.

* `ENABLE_SENTRY`: use Sentry service for error monitoring

### License

This project is licensed under the GNU Affero General Public License. You're free to use this project however you want as long as you keep it open source. For more details, [read the complete LICENSE file](https://github.com/kiwec/osu-ranked-lobbies/blob/master/LICENSE)
