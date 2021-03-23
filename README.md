## About
A PHP 8 playground, provided with an Apache 2.4 webserver. 

## Usage

### Initial
First time you want to use the container or rebuild it, after it was deleted.
```shell
docker build -t pg8 .
docker run -p 80:80 --name pg8 -v data:/var/www/html pg8
```

### Boot
If the container was already built in the past and you just want to start it.
```shell
docker run -p 80:80 pg8
```

### Rebuild
If something in _Dockerfile_ was changed, remove the built container, so it can be rebuild the next time   
```shell
docker stop pg8 && docker rm pg8
```
Now run the **Initial** command.

### SSH
```shell
docker exec -it pg8 bash
```  
  
  
  

## Miscellaneous

### PHP 8 native installed modules
```
[PHP Modules]
Core
ctype
curl
date
dom
fileinfo
filter
ftp
hash
iconv
json
libxml
mbstring
mysqlnd
openssl
pcre
PDO
pdo_sqlite
Phar
posix
readline
Reflection
session
SimpleXML
sodium
SPL
sqlite3
standard
tokenizer
xml
xmlreader
xmlwriter
zlib
```