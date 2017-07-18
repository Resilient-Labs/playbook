*Make sure you follow the instructions for* [Wordpress](wp.md) *and get your environment up before installing.*

# Composer Set-up

Install Homebrew on your Mac:

```shell
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Then install PHP:

```shell
brew update
brew tap homebrew/dupes
brew tap homebrew/php
brew install php71
brew install composer
```
To test installation, run:
```shell
composer -v
```
The terminal response should look like the following:
```shell
Composer version 1.1.2 2016-05-31 19:48:11 (or whatever the latest version is - you will have to scroll upward to find it)
```

Download these files and unzip them:

[GitHub Updater](https://github.com/afragen/github-updater/releases)

[WP-Sync-DB](https://github.com/wp-sync-db/wp-sync-db/releases)

[WP-Sync-DB Media Files](https://github.com/wp-sync-db/wp-sync-db-media-files)

### WP SYNC DB/DB Media Files Install

Make sure you’re in the /site directory:

```shell
cd ../site
```
pwd

*Output Example => /Users/desktop/rlab/myProject/site*
(should pop up upon entering the command)

Use Composer to install WP Sync DB:
```shell
composer require wp-sync-db/wp-sync-db:dev-master@dev
```
Use Composer to install the media attachments plugin for WP Sync DB:
```shell
composer require wp-sync-db/wp-sync-db-media-files:dev-master
```

Always always ALWAYS run the following to keep your Composer up-to-date:
```shell
composer update
```

*GITHUB UPDATER Install*
#### Note: This will automatically update your GitHub-based plugins to their newest versions. Not a necessity, but highly recommended.

Run the composer command:
```shell
composer require afragen/github-updater
```
###### Upload

* Download the latest tagged archive (choose the "zip" option).
* Unzip the archive, rename the folder correctly to github-updater, then re-zip the file.
* Go to the Plugins -> Add New screen and click the Upload tab.
* Upload the zipped archive directly.

###### Manual Alternative

* Download the latest tagged archive (choose the "zip" option).
* Unzip the archive, rename the folder to ```github-updater```.
* Copy the folder to your ```/wp-content/plugins/``` directory.

When all of this is done, run your Vagrant environment and go to the dashboard of your local Wordpress site. Go to ```Plugins``` and activate WP Sync DB and its media attachment, and GitHub Updater.
