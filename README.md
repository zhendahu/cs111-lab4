# Hey! I'm Filing Here

This program creates an ext2 filesystem with a root directory, lost and found directory, a hello-world file, and a symlink.

## Building

To build this program, run the command 

```
make
```

within the directory.

## Running

To compile:
```
make
./ext2-create
```

To mount:
```
mkdir mnt
sudo mount -o loop cs111-base.img mnt
```

Example output of `ls -ain`:

```
ls -ain
$ total 7
$      2 drwxr-xr-x 3    0    0 1024 Nov 30 02:59 .
$ 942253 drwxr-xr-x 5 1000 1000 4096 Nov 30 02:59 ..
$     13 lrw-r--r-- 1 1000 1000   11 Dec 31  1969 hello -> hello-world
$     12 -rw-r--r-- 1 1000 1000   12 Dec 31  1969 hello-world
$     11 drwxr-xr-x 2    0    0 1024 Nov 30 02:59 lost+found
```
## Cleaning up

To unmount:
```
sudo umount mnt
```

To remove the mount directory:
```
rmdir mnt
```

To clean up binary files:
```
make clean
```