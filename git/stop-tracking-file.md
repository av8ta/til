# stop tracking a file in git that you've already committed

Add it to `.gitignore` and then

```sh
git rm --cached /path/to/file
```
