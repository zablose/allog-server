# Allog Server

> Check Allog's [readme](https://github.com/zablose/allog/blob/master/readme.md) for more details.

## Development

> Check submodule's [readme](https://github.com/zablose/docker-damp/blob/master/readme.md) for more details about
> development environment used.

### Hosts

Append to `/etc/hosts`.

```
127.0.0.1       allog-server.zdev
127.0.0.1       www.allog-server.zdev
```

### Quick Start

    $ git clone -b 'dev' --single-branch --depth 1 https://github.com/zablose/allog-server.git allog-server
    $ cd allog-server
    $ git submodule update --init
    
    # Copy env file, then ammend it to your needs.
    $ cp .env.example.dev .env
    
    # Copy setup file, then ammend it to your needs.
    $ cp damp-post-setup.example.sh damp-post-setup.sh
    
    $ docker-compose -p zdev up -d
    
    # To see post-script logs, while container is starting.
    $ tail -f docker-damp/logs/all.log
    
    # To enter container, using Bash shell.
    $ docker exec -it allog-server-damp bash

## License

This package is free software distributed under the terms of the MIT license.
