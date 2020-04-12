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
