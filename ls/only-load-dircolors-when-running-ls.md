# load dircolors only for ls and only when stdout is not a terminal

Create a shell script at `~/bin/ls`

```sh
#!/bin/sh

if [ -t 1 ]; then
  eval $(dircolors -b ~/.dir_colors)
fi
exec /bin/ls "$@"
```