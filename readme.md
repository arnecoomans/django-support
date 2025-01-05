# Django Support Repository

This repository contains data and scripts that support running django projects.

## update.sh
Update.sh is a shell script that handles updating the django project on the remote host.
It makes a git pull and based on the git output, takes the following actions
- Enable virtual env
- Installs requirements via pip
- Executes pending migrations
- Executes collectstatic
Then restarts the pool name (first segment of directory name, untill first . character)
via supervisorctl.
