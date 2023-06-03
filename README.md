## UID: 805820938

(IMPORTANT: Only replace the above numbers with your true UID, do not modify spacing and newlines, otherwise your tarfile might not be created correctly)

# Hey! I'm Filing Here

One line description of this code.
This is an implemenetation of the ext2 file system for a single block group, specificially with 3 directories a text file and a symlink.

## Building

Explain briefly how to build your program.
Untar the submission file using:
tar -xvf <805820938-lab4-submission>
cd into the new directory
Run the 'make' command to generate executables 

## Running

Show how to compile, mount, and example output of `ls -ain` your mounted
filesystem.
The following mounts the file system:
```bash
./ext2-create
mkdir mnt
sudo mount -o loop cs111-base.img mnt
```
On running 
```bash
ls -ain mnt
```
You should see:

```bash
ls -ain mnt
total 7
   2 drwxr-xr-x 3    0    0 1024 Jun  2 17:46 .
9274 drwxr-xr-x 5 1000 1000 4096 Jun  2 17:47 ..
  13 lrw-r--r-- 1 1000 1000   11 Jun  2 17:46 hello -> hello-world
  12 -rw-r--r-- 1 1000 1000   12 Jun  2 17:46 hello-world
  11 drwxr-xr-x 2    0    0 1024 Jun  2 17:46 lost+found
```

## Cleaning up

Explain briefly how to unmount the filesystem, remove the mount directory, and
clean up all binary files.
TO unmount the file system:
```bash
sudo umount mnt
rmdir mnt
```
Clean up the executables with:
```bash
make clean
```