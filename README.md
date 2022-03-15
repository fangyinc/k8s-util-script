# k8s-util-script

K8s scripts

## Docker batch scripts

**batch save docker images**

Suppose you have the following file:
```batch-images.txt```

```txt
busybox:1.28
aiotceo/pause:3.5

```

```shell
$ sh ./docker/save-batch.sh -l batch-images.txt -i batch-images.tar.gz
Image pull success: busybox:1.28
Image pull success: aiotceo/pause:3.5
Creating batch-images.tar.gz with 2 images
```
```batch-images.tar.gz``` is your images.

**batch load docker images**

```shell
$ sh ./docker/load-batch.sh -l batch-images.txt -i batch-images.tar.gz -r localhost:5000
```

