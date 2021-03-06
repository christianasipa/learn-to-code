# Crontab

This guide covers rules and examples for adding jobs to your _crontab_ schedule file.

Edit the schedule with `crontab -e`.

Tutorials:
- On [linoxide.com](https://linoxide.com/linux-how-to/schedule-job-linux-commands/)
- On [computerhope.com](https://www.computerhope.com/unix/ucrontab.htm)
- On [linuxize.com](https://linuxize.com/post/scheduling-cron-jobs-with-crontab/)
- [How to view results of crontobs](https://superuser.com/questions/122246/how-can-i-view-results-of-my-cron-jobs) on _superuser.com_.

## Times

Guide to time format. See `man crontab` for more details.

### Five stars time

```
* * * * *

* minute (0-59)
* hours (0-23)
* day (1-31)
* month (1-12)
* day of week (0 - 7 with Sunday as 0 and 7)
```

### Words

- `@hourly`
- `@daily`
- `@weekly`
- `@monthly`
- `@yearly`
- `@reboot` - On machine restart. You may want to add a sleep command in your script to wait a few minutes, unless this might be done automatically.

## File structure

This is an example of lines to include in a crontab file, setting environment and then jobs.

```
SHELL=/bin/bash
PATH=/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin

# m h dom mon dow  command
  0 * *   *   *    echo "test"
  * * *   *   1-4  path/to/file.sh

```

The default shell is `SHELL=/bin/sh`.

The default path is more limited than your login shell - it is set as `PATH=/usr/bin:/bin`.

The variable `MAILTO` can be set as well. It defaults to the current user (`my-user` which acts as `my-user@localhost`) but can be set to `''` to a comma-separated list.

You can also change the config values in between jobs.

```
MAILTO=my-user
@daily  echo 'Test!'

MAILTO=foobar@example.com
@daily echo 'Another test'
```

## Example jobs

- Disk usage
    - `0 * * * 1-5 du -h --max-depth=1 /`
- Run at 9:30am on Mondays and Thursdays. Activate virtual environment and run python script.
    - `30 9 * * 1,4 source activate myenv && cd path/to/folder && python report.py`
- Hide stdout output and redirect any errors to an error file.
    - `0 5 * * * /path/to/job.sh 1> /dev/null 2> /path/to/file.err`
- Send output to mail other than set in MAILTO.
    - `* * 2 * * /path/to/script.sh | /usr/bin/mail -s "My Subject" user@domain.com`
- Another mail example. Stdout is absorbed, then stderr is redirected to stdout and is then piped to mail.
    - `30 12 * * * /path/to/script.sh 1> /dev/null 2>&1 | mail -s "My Subject" user@domain.com`
- Send _stderror_ to mail address. This should be equivalent to the above but I've not tested.
    - `30 12 * * * /path/to/script.sh 1> /dev/null 2> mail -s "My Subject" user@domain.com`
