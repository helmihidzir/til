# Find and kill process

Find process with port number
```bash
lsof -i tcp:3000
```

Find process with name
```bash
ps -ax | grep <process name>
```

Kill process
```bash
kill -9 PID
```