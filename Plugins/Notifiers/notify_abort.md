---
import:
 - Includes/PluginReplacedArchived
removed_in_version: 2.9.0
replacement_plugins: '[notify](/Plugins/notify)'
---
# Notify Abort
{{> Includes/PluginReplacedArchived }}

Sends a notification to [notifer](/Plugins/Notifiers) plugins on task aborts.


### Config:

| Options |Type|  Description | Default |
| --- | ---| --- |---|
|**to**|list|List of at least one notifer plugins, the same plugin can be used 
### Usage:
```yaml
tasks:
  download_task:
    rss: http://stuff.com
    accept_all: yes
    download: /downloads/
    notify_abort:
      to:
        - pushover:
            user_key: user_key
```
This will send a notification using the following defaults:  
`title` -  `Task {{ task_name }} has aborted!`  
`message` - `Reason: {{ task.abort_reason }}`

You could also use `notify_abort` in a global template as such:
```yaml
templates:
  global:
    notify_abort:
      to:
        - pushover:
            user_key: user_key
```
Doing this will let you be notified of any task abort.