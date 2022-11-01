# Eggdrop Startup Scripts (1.0.0)
Startup scripts for the Eggdrop IRC Bot - uses the "screen" command to manage a session. This also restarts the Eggdrop process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/EggdropStartup) - [Official Forum](https://eggdrop.retro-os.live/index.php/forum/our-eggdrop-utilities)  - [Official Download Area](https://eggdrop.retro-os.live/index.php/downloads/category/27-our-eggdrop-utilities)

---
These start up the Eggdrop bot at boot time with a "screen" process.

1. Copy **eggdrop** into **/home/eggdrop/bin** - make sure it is executable
2. Copy **starteggdrop** into **/home/eggdrop/eggdrop** - make sure it is executable
3. Put **@reboot /home/eggdrop/bin/eggdrop start** into your crontab

When you want to view the Eggdrop console, just enter "**screen -r**" in your shell.

To disconnect from the Eggdrop console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 20.04 server...

If you want to turn off the bot respawning type "**touch /home/eggdrop/eggdrop/nostart**". To reenable it type "**rm /home/eggdrop/eggdrop/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
