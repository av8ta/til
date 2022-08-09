# restart jobs on system boot

when your cloud server goes down it's great when it restarts jobs when it comes back up!

pm2 doesn't do this out of the box but it's easy to setup

## start pm2 at boot

systemd|upstart|launchd|rcd|systemv

```sh
pm2 startup <init-system>
```

if you don't know what init system your server uses just leave it off the command and pm2 will detect it: `pm2 startup`

pm2 configures your init system for you. now it will start on boot, but it won't start jobs yet...

## start jobs on boot

in order to start jobs on boot you just need to save those jobs.

start your jobs with pm2 and then save them, and that's all you have to do :)

```sh
pm2 start some-job.js
pm2 save
```
