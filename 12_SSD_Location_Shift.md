

Okay so update I though I new where the SSD was mounted but I was incorrect lol


Run:
```
lsblk
```

This is a sample of what it should kinda look like:
```
NAME        MAJ:MIN  RM   SIZE RO TYPE MOUNTPOINTS
sda           8:0    0 465.8G  0 disk
└─sda1        8:1    0 465.8G  0 part /media/YOUR-USERNAME/NAME-OF-SSD
mmcblk0     179:0    0  59.5G  0 disk
├─mmcblk0p1 179:1    0   256M  0 part /boot/firmware
└─mmcblk0p2 179:2    0  59.2G  0 part /

```

And then look at the "MOUNTPOINTS" column where `sda1` (your ssd) is.  
That is where you want to put the files you want in your SSD.

<br>

Unfortunately I thought my ssd was in `/mnt/ssd` so in my past tutorials I was referring to this.  
Just that that into account when reading!  

To move files, use:
```
sudo mv [original path] [updated path]
```

I am currently doing this with my files from `/mnt/ssd` and now I am putting it in the new path


Now how can I used, available, and total for EVERY drive:
```
df -h
```
df = disk free
-h = human readable (Show sizes in KB/MB/GB instead of bytes)