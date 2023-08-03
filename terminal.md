# Useful Terminal Commands

## nano

- nano +12 file
    - Goes to line 12

- Go to beginning of line
    - ctrl+a

- Go to end of line
    - ctrl+e

## Apachectl -k __ (Debian)

apache recommends apachectl -k vs service

stop
: kills all of its threads and exits

graceful (equivalent to service apache2 reload)
: advise it threads to exit when idle, then apache reloads the configuration (it doesn't exit itself)

restart (equivalent to service apache2 stop; service apache2 start)
: kills all of its threads, then the apache reloads the configuration file, rather than killing itself (similar to graceful)

graceful-stop
: like graceful, but instead of reloading the configuration, it will stop responding to new requests

## systemctl vs service

systemctl
- "low-level"
- higher control

service
- "high-level"
- abstracts various service managers
   - service redirects to systemctl on centos7

get loaded php configuration
1) `sudo -i`
2) `php --ini`
3) Get location of `Loaded Configuration File`
4) If there is a cli listed in path, php is loaded for command line interface

## Change php version

1) `cd /usr/bin`
2) `php -v`
3) `mv php php` then add x.y version number from step 2
4) `mv phpx.y php`
5) `php -v`

## Find directory

`find . -type d | grep DIRNAME`