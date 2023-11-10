# ubuntu-volume-savers

## Configuration

**snap.clean.sh**: This script is used to remove disabled snap packages.  
**tmp.clean.sh**: This script removes temporary files that are older than one day.

## Usage

To use these scripts, you need to run them with sudo. Here's how you can do it:

Execute the script as a superuser: `sudo bash {filename}.sh`

## Automation

For automatic periodic cleaning, it's recommended to add a cron job. Here's an example cron entry to run tmp.clean.sh every 12 hours.  
Add the following to the bottom of your /etc/crontab file to automatically run the script. (sudo vim /etc/crontab)

```bash
0 */12 * * * root /home/{username}/ubuntu-volume-savers/tmp.clean.sh
```

Replace {username} with your actual user name on your system.
