###### [main](README.md)
Plan B: Updraft
===============

For whatever reason, be it the troubleshooting taking too long for the rest of the Wordpress playbook or some other lack of time, you've come to Plan B - fortunately, it is a very quick process to make sure your site is live and on time.

## Setting Up The Server For Staging

See [this documentation](github.md) for setting up the server.

## From Local To Live

- Get a key from the Live Wordpress Site
- Go to ```Settings > UpdraftPlus Backups```
- Click ```Clone/Migrate```
- Put the key in the second section and click ```Add Site```
- The site url or IP address should show up directly beneath the field you just put the key in. Select that site and click ```Send```. You will not need to put in the site key again, and can select the site directly from this field.
- Make sure all boxes are checked, then click ```Send```
- NOW WAIT FOR IT TO FINISH ITS BACKUP JOB

## Live Cloning

- Go to the live version of the site and click ```Settings > UpdraftPlus Backups```
- Click ```Clone/Migrate``` and select the backup you want to clone - you'll find it based on its date
- Click ```Clone``` and make sure ALL boxes are checked
- Click ```Delete Old Directories``` and repeat the first three steps
- If the site requires you to log in again, do so.
- Voila, the site is up-to-date
