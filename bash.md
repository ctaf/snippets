#### Repeat a command until success.

**Code:**

```
until !!; do done
until !!; do sleep 5; done
``` 

**Sources:**

http://www.commandlinefu.com/commands/view/12327/retry-the-previous-command-until-it-exits-successfully

---

#### Battery saving mode for graphics. 
**Code:**

`echo battery | sudo tee /sys/class/drm/card0/device/power_dpm_state` 

**Sources:**

https://wiki.ubuntuusers.de/Grafikkarten/AMD/radeon

http://askubuntu.com/questions/324733/how-to-enable-the-radeon-dynamic-power-management-feature

**Notes:**

Do this regularly or put into rc.local.

On newer kernels (> 3.11), only makes sense in combinations with a boot
parameter: `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash radeon.dpm=1"`

---

#### Change keyboard layout via terminal.
**Code:**

`setxkbmap {de|us}` 

**Notes:**

Might interfere with keyboard switcher of desktop environment (e.g. Cinnamon).

---

#### One-line bandwidth test
**Code:**

`wget http://cachefly.cachefly.net/400mb.test -O /dev/null` 

**Sources:**

https://danielmiessler.com/blog/command-line-bandwidth-test/

**Notes:**

Cachefly is the world’s fastest CDN with the most hops, so no matter where you are you’ll be able to get a true test of your connection by seeing how quickly you can pull from it.
