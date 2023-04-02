dnf update

gdisk /dev/sdb
Konfig Partitionen

lsblk

vgs
pvs
lvs

pvcreate /dev/sdb1

pvdisplay
lvdisplay

smartctl // überlebensdauer

vgchange

lvchange

vgextent data /dev/sdb1 /dev/sdc1

// Fs formatieren
mkfs.ext4 /dev/mapper/data-primary
mkfs.ext4 /dev/mapper/data-backup

/etc/fstab

