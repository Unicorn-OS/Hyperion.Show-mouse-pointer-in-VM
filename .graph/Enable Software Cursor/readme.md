# Solution
This works!
https://superuser.com/questions/1546702/qemu-no-visible-cursor-when-using-qxl-or-virtio

> For anyone who’s interested, this how I enabled the software cursor:

```
echo '''Section "Device"
  Identifier "graphicsdriver"
  Option     "SWcursor" "on"
EndSection''' | sudo tee /etc/X11/xorg.conf.d/vesa-swcursor.conf
```
more:
- https://www.reddit.com/r/linuxquestions/comments/21h663/comment/cgewt03/

# Doesn't work in QXL Displays
Works in:
- VGA

# Research:
sch: https://www.google.com/search?q=virt-viewer+swcursor

bug:
- [No mouse cursor in Spice/QXL-enabled guests](https://bugzilla.redhat.com/show_bug.cgi?id=985461)
