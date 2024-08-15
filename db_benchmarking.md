# Db benchmarking


## Sysbench

```
sudo apt install sysbench
sudo brew install sysbench
```

## Iozone

```
docker run -it threadx/docker-ubuntu-iozone
iozone -R -l 5 -u 5 -r 4k -s 100m -F /home/f1 /home/f2 /home/f3 /home/
```
