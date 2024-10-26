## chmal command

### Summary

You can change your message of the day after log-in

### Description

If you don't like the default message of the day after log-in that is generated by the kernel, then you can use this command to change the message and store it permanently on the config file.

It also has placeholder support, like if you have `<shortdate>` and `<longtime>` placeholders, the `<shortdate>` placeholder changes to the current system date in the MM/DD/YYYY form, and the `<longtime>` placeholder changes to the current system time in the HH:MM:SS AM/PM form. More information about placeholders are available [Placeholders](../../misc/Placeholders.md).

If no arguments are specified, the text editor shell will open to the path of MAL text file.

### Command usage

* `chmal [message]`

### Examples

* `chmal`: It takes you to the text editor shell opened at the path of MAL text file.
* `chmal This computer is turned on at <shortdate> <shorttime>`: It changes your MOTD after login to the message specified, with the placeholders included in the message.
* `chmal Welcome to the kernel, <user>! Your system time zone is <timezone>`: It changes your MOTD after login to the message specified, with the `<timezone>` placeholder included in the message to get current standard time zone.