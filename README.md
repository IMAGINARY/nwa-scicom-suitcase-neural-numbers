# tu-delft-suitcase-neural-numbers

Neural Numbers as a suitcase exhibit for TU Delft.

An installation-specific mod of the 
[Neural Numbers Mini](https://github.com/IMAGINARY/neural-numbers-mini) exhibit.

## Installation

Run

```bash
npm install
npm run build
```

to build the project. The built files are in the `dist` directory.

## Configuration

The default configuration can be overriden through `extras/config.json` file.  As of this writing, 
applying a new configuration requires recompiling the project 🤨.

## Sentry

This project uses [Sentry](https://sentry.io) to track errors in production.

Unhandled exceptions and console.error messages will be sent if the Sentry DSN is set.

The Sentry DSN will be read from:
- The `sentry-dsn` query string argument. (Read from the browser)
- The `sentryDSN` key in config.json. (Read at build-time only)
- The `SENTRY_DSN` environment variable. (Read at build-time only)

To enable Sentry, set the `SENTRY_DSN` environment variable to your Sentry DSN.

## Idle timeout

The app will automatically close the training panel after a period of inactivity.

The timeout duration (in seconds) can be set through:
- The `idle-timeout` query string argument. (Read from the browser)
- The `idleTimeout` key in config.json. (Read at build-time only)
- The `IDLE_TIMEOUT` environment variable. (Read at build-time only)

The default value is 60 seconds.  Set to 0 to disable the timeout.

## Credits

Adapted by [Eric Londaits](https://github.com/elondaits)
from the [Neural Numbers](https://github.com/IMAGINARY/neural-numbers)
exhibit created by [Aaron Montag](https://github.com/montaga) for IMAGINARY gGmbH.

## License

Copyright 2019-2025 IMAGINARY gGmbH.
Licensed under the MIT License (see LICENSE).

