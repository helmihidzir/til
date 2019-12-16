# Bundle permission error

If you run into this error,
```
There was an error while trying to write to `/var/www/code/.bundle/config`. It
is likely that you need to grant write permissions for that path.
```
try running `sudo chmod -R 777 /var/www/code`

---

To make secure or lock permission run, `sudo chmod 600 /var/www/code`