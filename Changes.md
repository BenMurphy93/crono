2.0.1
-----------
- Changes to Web UI colouring - moved to a dark mode-esque feel
- Removed "log" link from Jobs index and added the link to Job ID
- Ordered the Jobs index by last performed at, descending
- Split the jobs index job id into 2 columns to provide better job context
- Fixed :memory filename to allow the gem to work with windows (version tidyup)
- JS added to autoscroll to the bottom of logs
- Added a link back to the main app within layout (uses Rails.application.class to get App name)

2.0.0
-----------
- Converted this gem to a proper Rails engine
- Gets rid of `sinatra` and `haml` dependencies for the Web UI
- Web UI is now responsive and thus usable on smartphones, etc.
- Fixed crash with Ruby 3.0


1.1.0
-----------
- Rails 3 and old Rubies are not supported anymore, sorry rails 3 guys...
- Requires Ruby 2.2.2 or newer
- Fixed crash when no jobs defined in your cronotab
- Some doc updates (thanks to @pachacamac)
- Job will schedule on: today if at: time not passed (thanks to @acolyer)
- Job log truncating (thanks to @reiz)


1.0.3
-----------
- "every 1 week" jobs now displaying on Rails 5 as "1 week" not as "7 days"
- Liberal gem dependencies to support both Rails 4 and Rails 5


1.0.2
-----------
- Fix table_name_suffix/prefix issue: https://github.com/plashchynski/crono/issues/33


1.0.1
-----------
- Fix job saving


1.0.0
-----------
- Rails 5 support (thanks to @adamico)
- Possibility to schedule jobs with arguments (thanks to @preisanalytics)
- Added :within option to run only within given time interval (thanks to @lhz)
- daemon gem support (thanks to @preisanalytics) https://github.com/plashchynski/crono/pull/37
- Support multiple nodes (thanks to @Natural-Intelligence)
- Fixed DB connection pool issue (thanks to @ChandravatiSG)


0.9.1
-----------
- Add ability to define minimal time between job executions to support multiple corno nodes, so two different nodes will not execute the same job


0.8.9
-----------

- We moved Web UI to materializecss.com CSS framework
- We moved from CDN to local assets for Web UI
- We show current state of a job in Web UI (thanks to @michaelachrisco) https://github.com/plashchynski/crono/issues/16
- We won't write a pidfile unless daemonized (thanks to @thomasfedb) https://github.com/plashchynski/crono/pull/13
- Fixed `rake crono:clean` task error
- Fixed issue when jobs scheduled at same time exclude each other https://github.com/plashchynski/crono/issues/19
- Fixed issue with a daemon crash due to `time interval must be positive` error


0.8.0
-----------

- Added `on` (day of week) option to cronotab.rb semantic
- Added job health check and job health indicator to the Web UI


0.7.0
-----------

- Added simple Web UI


0.6.1
-----------

- Persist job state to your database.


0.5.2
-----------

- Fix: Scheduled time now related to the last performing time.


0.5.1
-----------

- Added -e/--environment ENV option to set the daemon rails environment.


0.5.0
-----------

- Initial release!
