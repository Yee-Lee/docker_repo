# docker_repo

# eebasket

## Environment
* wordpress: 
    image: fpm-apline
    volume: mounted root in volumes/wordpress/

* mysql:
    image: latest
    volume: mounted database in volumes/db_data

* nginx: 
    (option-1)
    image: compiled by dockerfile
    volume: share the folder with the wordpress root
    config: copy from nginx.config

    (option-2)
    image: latest
    volume: share the folder with the wordpress root
    config: use default config and includes the customized configs in conf.d/

.env:
    The password and username used for mysql. You can modify this for your case after pull. 

## Note

    1. http://<your_site>:8089
    2. Wait couples of minutes that wordpress copying files before the homepage showing up.

