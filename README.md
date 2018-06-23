# Getting started #

Please read this section espacially if you are unfamiliar with Docker.

## Docker ##

### Installation ###

To install Docker itself please download and install package from [docker.com](https://www.docker.com/products/overview).

### Usage ###

To boot Docker, run command from project's root directory:

```
#!bash

docker-compose up
```

After finished work it's good to stop all project's containers with command:

```
#!bash

docker-compose stop
```

While container is working you can use WP-CLI commands, like this:

```
#!bash

docker-compose run --rm wpcli wp --info
```

# Repository stucture #

* `/` - root directory where all enviroment files resides
* `/public/` - not editable, ignored files, contains WordPress core
* `/plugins/` - contains project plugins in directories mapped to specific ones in `/public/wp-content/plugins/`
* `/themes/` - contains project themes in directories mapped to specific ones in `/public/wp-content/themes/`
* `/docker-compose.yml` - Docker project configuration file
* `/wp.sh` - this file runs everytime you run `docker-compose up` command and it's used to keep WordPress dependencies
