# Redmi-Pad-Pro-Dizi-AutoInstaller-lineage-os
all thanks and credits to:
https://github.com/MisterZtr/LineageOS_gsi
open the website for the guide: https://tokiw0-3.github.io/Redmi-Pad-Pro-Dizi-AutoInstaller-lineage-os/
in the releases is a zip with all the files needed just extract them to a convenient folder
## Updating (23.0 → 23.2, no data wipe)

If LineageOS 23.0 is already installed and you want to update to 23.2 (2026.05.24):

```
fastboot reboot fastboot
fastboot flash system LineageOS-23.2-20260524-GAPPS-EXT4-GSI.img
fastboot reboot
```

If space is insufficient, delete product logical partitions first:
```
fastboot delete-logical-partition product_a
fastboot delete-logical-partition product_b
```
Then retry the flash.

> First boot may take 5–15 minutes. If it bootloops, wipe data and clean-flash.
> Do **not** use `flash.bat` for updating — it wipes data.
