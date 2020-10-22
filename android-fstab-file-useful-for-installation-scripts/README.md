<blockquote code-like>
# Android fstab file.
#src mnt_point type mnt_flags and options fs_mgr_flags
# The filesystem that contains the filesystem checker binary (typically /system) cannot
# specify MF_CHECK, and must come before any filesystems that do specify MF_CHECK


/dev/block/platform/15570000.ufs/by-name/system	/system	ext4	ro	wait
/dev/block/platform/15570000.ufs/by-name/cache	/cache	ext4	noatime,nosuid,nodev,nomblk_io_submit,errors=panic	wait
/dev/block/platform/15570000.ufs/by-name/userdata	/data	ext4	noatime,nosuid,nodev,nomblk_io_submit,noauto_da_alloc,errors=panic	wait
/dev/block/platform/15570000.ufs/by-name/kernel	/kernel	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/ramdisk	/ramdisk	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/recovery	/recovery	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/ldfw	/ldfw	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/dtb	/dtb	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/dtb_backup	/dtb_backup	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/custom	/custom	ext4	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/efs	/efs	ext4	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/misc	/misc	emmc	defaults	defaults
/dev/block/platform/15570000.ufs/by-name/bootlogo	/bootlogo	emmc	defaults	defaults
/dev/block/sdb	/bootloader	emmc	defaults	defaults
#/dev/block/mmcblk0p1	/sdcard	vfat	defaults	voldmanaged=sdcard:auto
/dev/block/platform/15570000.ufs/by-name/bootimg	/boot	emmc	defaults	defaults
/dev/block/ram0        /ram0   vfat    defaults		wait
/dev/block/mmcblk0*        /storage/sdcard1   auto    defaults		wait
</blockquote>

