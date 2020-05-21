# README

A simple remote Raspberry based platform/procedures/whatever to control under-development platformio/Arduino projects. Goals:

- store Arduino projects serial logs for debugging purposes
- re-program them remotely if required
- reset them remotely if required

## Steps

0. (optional) Install `Raspbian` in your `Raspberry PI Zero W` (or any Raspberry you like).
1. Install `platformio-core`
2. Schedule hourly the script `hourly-cron`.
```
0 * * * * /path/to/devino/hourly-cron
```

# Device logs

Under directory `devlogs`.

Make sure that `hourly-cron` is correctly installed (see README.md).

## About logrotate standard installation 

The tool `logrotate` runs daily thanks to:

```
/etc/cron.daily/logrotate
```

Unfortunately you cannot add symlinks to `/etc/logrotate.d/` where the system would perform the log rotation without much effort.

