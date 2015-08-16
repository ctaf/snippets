#### Battery saving mode for graphics. 
**Code:**

`echo battery | sudo tee /sys/class/drm/card0/device/power_dpm_state` 

**Sources:**

https://wiki.ubuntuusers.de/Grafikkarten/AMD/radeon

http://askubuntu.com/questions/324733/how-to-enable-the-radeon-dynamic-power-management-feature

**Description:**

Do this regularly or put into rc.local.

On newer kernels (> 3.11), only makes sense in combinations with a boot
parameter: `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash radeon.dpm=1"`
