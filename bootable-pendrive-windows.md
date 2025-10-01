# Bootable pendrive for Windows installation

Notes on how to config a bootable pendrive to be used for a Windows installation. This process uses the `diskpart` tool that comes by default in Windows distributions.

## Pendrive setup

Init diskpart
```
diskpart
```

List all available disks
```
list disk
```

Select the disk corresponding to the pendrive (in this case id is 1)
```
select disk 1
```

Clean disk
```
clean
```

Create the primary partition
```
create partition primary
```

Format disk, could be ntfs/fat32/exfat
```
format fs=fat32 quick
```

Done! Exit diskpart
```
exit
```

## ISO

Download the desired Windows ISO from the official website. Mount the ISO, and copy the ISO's content into the pendrive root folder. After that, pendrive should be ready to be used for a windows installation.