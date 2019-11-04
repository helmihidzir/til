# Run sidekiq command

Normal command
```bash
bundle exec sidekiq -q default
```

Command for background mailer
```bash
bundle exec sidekiq -q default -q mailers
```