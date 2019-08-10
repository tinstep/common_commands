### BTRFS
``` btrfs fi show ```
```
Label: none  uuid: 58bd01a7-f160-4fea-aed3-c378c2332699
        Total devices 6 FS bytes used 7.36TiB
        devid    1 size 2.73TiB used 2.61TiB path /dev/sda
        devid    2 size 2.73TiB used 2.61TiB path /dev/sdd
        devid    3 size 3.64TiB used 2.61TiB path /dev/sdf
        devid    4 size 2.73TiB used 2.61TiB path /dev/sdb
        devid    5 size 2.73TiB used 2.61TiB path /dev/sdc1
        devid    6 size 3.64TiB used 2.61TiB path /dev/sde
```

Show device errors

```sudo btrfs device stats /share```

Show errors and reset stats on device

```sudo btrfs scrub stats -z /dev/sdf```

Fix bitrot - can select folder

```sudo btrfs scrub start /share```

Show progress

```sudo btrfs scrub status /share```

Defrag

```btrfs filesystem defragment [btrfs filesystem path] ```


Add Device
``` btrfs device add -f /dev/sd[x] [btrfs mount point]  ```

Remove Device

```btrfs device delete /dev/sd[x] [btrfs mount point]```

Alternatively, if a device is missing:

```btrfs device delete missing [btrfs mount point]```

***The array has to be on-line in order to delete a device. If your device has failed (and thus missing), then you need to mount the array in degraded mode before executing the command.***

Mount Array In Degraded Mode
```sudo mount -o degraded /dev/sd[x] [btrfs mount point]```

Create Subvolume

```btrfs subvolume create```

Show subvolumes

```btrfs subvolume list```

Take Snapshot

```btrfs subvolume snapshot```

Delete Subvolume

```btrfs subvolume delete```
