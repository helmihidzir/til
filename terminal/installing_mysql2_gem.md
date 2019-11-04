# Installing mysql2 gem

Version 0.4.6
```bash
gem install mysql2 -v 'o.4.6' -- --srcdir=/usr/local/mysql/include
```

Version 0.5.2 MacOS Mojave
```bash
brew install openssl
gem install mysql2 -v '0.5.2' -- --with-ldflags=-L/usr/local/opt/openssl/lib --with-cppflags=-I/usr/local/opt/openssl/include
```
[Source](https://gist.github.com/fernandoaleman/ee3ac6957c2ba4f7d7d33a251d58b191)