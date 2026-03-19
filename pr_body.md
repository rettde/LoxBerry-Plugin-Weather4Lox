## Summary

Fixes multiple bugs in the weather4lox-version4 branch. All changes tested on a live LoxBerry system.

## Fixes

- [#122](https://github.com/mschlenstedt/LoxBerry-Plugin-Weather4Lox/issues/122): All Perl scripts use `filename` + `append => 1` instead of `logdir` to prevent unbounded log file creation on ramdisk
- [#119](https://github.com/mschlenstedt/LoxBerry-Plugin-Weather4Lox/issues/119): Correct `$icon`/`$code` order in interpolated hourly data (`grabber_openweather.pl`)
- [#40](https://github.com/mschlenstedt/LoxBerry-Plugin-Weather4Lox/issues/40): Replace deprecated `LoxBerry::Web::readlanguage` with `LoxBerry::System::readlanguage`

## Other improvements

- `show.cgi`: Graceful error message instead of `die` when `.dat` files not yet available
- `datatoloxone.pl`: Copy generated HTML files and `index.txt` to web-accessible dirs after creation
- `datatoloxone.pl`: Remove MQTT password from debug log output (security)
- `datatoloxone.pl`: Fix double semicolon
- `daemon`: Copy HTML files and `index.txt` to web dirs at boot
- `grabber_openweather.pl`: Fix wrong variable in error message, double semicolon
- `index.cgi`: Remove duplicate WUGRABBER config line
