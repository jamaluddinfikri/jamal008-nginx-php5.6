# This image contains nginx and php5.6 using the alpine linux 3.4 base.

## Service :
    - nginx
    - php5.6

## The default environment is there and you can customize it yourself:
```
ENV PHP_FPM_USER="www"
ENV PHP_FPM_GROUP="www"
ENV PHP_FPM_LISTEN_MODE="0660"
ENV PHP_MEMORY_LIMIT="128M"
ENV PHP_MAX_UPLOAD="50M"
ENV PHP_MAX_FILE_UPLOAD="20"
ENV PHP_MAX_POST="100M"
ENV PHP_DISPLAY_ERRORS="On"
ENV PHP_DISPLAY_STARTUP_ERRORS="On"
ENV PHP_ERROR_REPORTING="E_COMPILE_ERROR\|E_RECOVERABLE_ERROR\|E_ERROR\|E_CORE_ERROR"
ENV PHP_CGI_FIX_PATHINFO=0
ENV TIMEZONE="Asia/Jakarta"
```

## how to use it without a custom environment:
```
docker run -d --name nginx -p 80:80 jamal008/nginx-php5.6
```

## how to use it by adding a custom environment:
```
docker run -d --name nginx -p 80:80 -e TIMEZONE="Asia/Jakarta" jamal008/nginx-php5.6
```
\
\
repo build Github: [link](https://github.com/jamaluddinfikri/jamal008-nginx-php5.6)\
repo docker hub: [link](https://cloud.docker.com/u/jamal008/repository/docker/jamal008/nginx-php5.6)

