## Installation

The installation of this add-on is pretty straightforward and not different in
comparison to installing any other Home Assistant add-on.

1. [Add our Hass.io add-ons repository][repository] to your Hass.io instance.
1. Install the "Home Panel" add-on.
1. Configure the "Home Panel" add-on. (See below)
1. Start the "Home Panel" add-on.
1. Check the logs of the "Home Panel" add-on to see it in action.
1. Click "Open Web UI".
1. Create a new account.
1. Once logged in, log into Home Assistant via the sidebar.
1. Please see [here][config] for how to configure Home Panel

**NOTE**: Do not add this repository to Hass.io, please use:
`https://github.com/hassio-addons/repository`.

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

Example add-on configuration:

```yaml
log_level: info
ssl: true
certfile: fullchain.pem
keyfile: privkey.pem
```

### Option: `log_level`

The `log_level` option controls the level of log output by the addon and can
be changed to be more or less verbose, which might be useful when you are
dealing with an unknown issue. Possible values are:

- `trace`: Show every detail, like all called internal functions.
- `debug`: Shows detailed debug information.
- `info`: Normal (usually) interesting events.
- `warning`: Exceptional occurrences that are not errors.
- `error`:  Runtime errors that do not require immediate action.
- `fatal`: Something went terribly wrong. Add-on becomes unusable.

Please note that each level automatically includes log messages from a
more severe level, e.g., `debug` also shows `info` messages. By default,
the `log_level` is set to `info`, which is the recommended setting unless
you are troubleshooting.

### Option: `ssl`

Enables/Disables SSL (HTTPS) on the app. Set it `true` to enable it,
`false` otherwise.

### Option: `certfile`

The certificate file to use for SSL.

**Note**: _The file MUST be stored in `/ssl/`, which is the default_

### Option: `keyfile`

The private key file to use for SSL.

**Note**: _The file MUST be stored in `/ssl/`, which is the default_



[banner]: https://raw.githubusercontent.com/timmo001/home-panel/master/docs/resources/banner.png
[buymeacoffee-shield]: https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-2.svg
[buymeacoffee]: https://www.buymeacoffee.com/timmo
[discord-shield]: https://img.shields.io/discord/478094546522079232.svg
[discord]: https://discord.me/hassioaddons
[docs]: https://github.com/hassio-addons/addon-home-panel/blob/v1.7.1/README.md
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg
[forum]: https://community.home-assistant.io/t/home-panel-a-touch-compatible-webapp-for-controlling-the-home/62597?u=timmo001
[hass]: https://www.home-assistant.io/
[home-panel]: https://github.com/timmo001/home-panel
[maintenance-shield]: https://img.shields.io/maintenance/yes/2020.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[release-shield]: https://img.shields.io/badge/version-v1.7.1-blue.svg
[release]: https://github.com/hassio-addons/addon-home-panel/tree/v1.7.1
[screen-configuration-main]: https://raw.githubusercontent.com/timmo001/home-panel/master/docs/resources/screen-configuration-main.png
[screen-main]: https://raw.githubusercontent.com/timmo001/home-panel/master/docs/resources/screen-main.png
[showcase-purple-space]: https://raw.githubusercontent.com/timmo001/home-panel/master/docs/docs/showcase/timmo/purple-space.png
