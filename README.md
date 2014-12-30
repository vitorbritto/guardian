![Guardian Logo](src/guardian.jpg "Guardian")


## Welcome

Guardian is a simple method to execute your backups with Rsync for external volumes in your local environment.


## Installation

> This script works only for *nix users! :)

```bash

# 1. Clone this repository
$ git clone git://github.com/vitorbritto/guardian.git

# 2. Place the `guardian.sh` script wherever you want

# 3. Make the script executable
$ chmod u+x path/to/guardian.sh

```


## Usage

    $ ./guardian.sh


## Configuration

Open `guardian.sh` and set your configurations.

    MAIN="$HOME/DIST/PATH/GOES/HERE"        # Destination / Output Folder
    SRC="$HOME/SRC/PATH/GOES/HERE"          # Source Files / Input Folder
    DIST="${MAIN}/BACKUP"                   # Backup directory
    LOGS="${MAIN}/LOGS"                     # Logs directory


## Bonus

### Adding an alias

If you prefer, put the following **alias** inside your `.bashrc` file:

    alias guardian="bash ~/path/to/script/guardian.sh"

Now, you can simply run:

    $ guardian

### Using Guardian with Crontab


- First of all, create a text file named `backup.txt`
- Insert: "00 6 * * 1 /path/to/script/guardian.sh && bash guardian.sh" in `backup.txt` file
- Now, simply execute `crontab backup.txt`
- That's it! Your cron job will work fine every week at 6:00 AM!

**Crontab Options:**
- crontab -e: edit the current job or create a new one
- crontab -l: list cron jobs
- crontab -r: remove a cron job

> Remember: you can set the time and desired period. For more information about crontab on Unix systems, [read this guide](http://ss64.com/bash/crontab.html).


## License

[MIT License](http://vitorbritto.mit-license.org/) © Vitor Britto
