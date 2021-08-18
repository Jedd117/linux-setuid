# linux-setuid
Simple script which can be used to execute a shell as root if you have access to load the binary as root via a cronjob, timer, etc.

## Info
If there's a scheduled event that will extract files as root, Then you can give this SUID exeecute permissions for all users to run this file as root. If you zip the file as root, then upload this to your target host, the permissions will remain. So giving the executable the following permissions would allow this to run as root:

```
chmod 6555 BINARY_NAME
```


# To compile

## 32 bit
  - `gcc -m32 -o setuid setuid.c`
## 64 bit
  - `gcc -o setuid setuid.c`

