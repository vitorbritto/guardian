![Guardian Logo](src/guardian.jpg "Guardian")


## Welcome

Guardian is a simple method to execute your backups with Rsync for external volumes.


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

    SRC="$HOME/Sites/"                  # Source directory
    MAIN="/Volumes/BACKUP"              # External Volume
    DIST="$MAIN/PROJECTS"               # Destination directory
    LOGS="_logs"                        # Logs directory
    EXCLUDE="$DIST/bkp_excludes.txt"    # Exclude list files on sync


## Bonus

If you prefer, put the following **alias** inside your `.bashrc` file:

    alias guardian="bash ~/path/to/script/guardian.sh"

Now, you can simply run:

    $ guardian


## License

[MIT License](http://vitorbritto.mit-license.org/) © Vitor Britto
