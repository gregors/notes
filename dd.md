# DD - data description aka disk destroyer

https://unix.stackexchange.com/questions/170768/what-does-dd-stand-for

## Copy hard disk 
```sh
# if - input filek
# of - output filek

dd if=/dev/sda of=/dev/sdb status=progress bs=1M 
````
