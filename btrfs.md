### BTRFS
<code> btrfs fi show </code>
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

show device errors

```sudo btrfs device stats /share```

Show errors and reset stats on device

```sudo btrfs scrub stats -z /dev/sdf```

fix bitrot - can select folder

```sudo btrfs scrub start /share```

show progress

```sudo btrfs scrub status /share```
