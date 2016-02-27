= Version Checker=

This plugin checks wether the user is running the latest version of flexget. To avoid unnecesary requests, this happens on an interval by default (1 request per day).
The plugin can be added to any task and output a log warning if it finds an update:
{{{
2016-01-06 17:56 WARNING  version_checker task1           You are not running latest Flexget Version. Current is 1.2.424.dev and latest is 1.2.423
}}}

'''Usages'''

There are 3 ways to use this plugin. The simplest is by calling it as a `bool`:
{{{
version_checker: yes
}}}
The default is a check once a day. To override that, user can run it with `always`, which will send the request for latest version on every execution:
{{{
version_checker: always
}}}
By default, the plugin will not check latest version if it detects that the user is running dev version. To override this, set it as an object:
{{{
version_checker:
  check_for_dev_version: yes
}}}
Alternatively, you can also set the interval (in days) for requests:
{{{
version_checker:
  interval: 7
}}}
