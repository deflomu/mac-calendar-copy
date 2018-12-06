# Calendar Copy Script

This scripts can be used to copy the contents of one calendar in the macOS
Calendar app to another calendar.

## How to use

:warning: Be careful: all events in the  destination calendar will be removed! :warning:

* Find the UUIDs of the calendars you which to copy by running the script `Calendar UUIDs.scpt`.
* Copy `config.plist-sample` to `config.plist` and enter the UUIDs.
* Run `Calendasync.scpt` to check that everything is working. This might take some time.
* Setup a cronjob to copy the calendars regularly. Example to run it every 3 hours:

    0 */3 * * * osascript /path/to/source/Calendersync.scpt

## Good to know

* Sometimes the Calendar.app will be unresponsive while the copy process is running.
* Sometimes the Calendar.app will not refresh the UI and Events will not be shown. Usually a restart of the app will fix this.

