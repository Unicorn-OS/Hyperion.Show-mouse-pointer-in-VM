# Solution
This works!
https://superuser.com/questions/1546702/qemu-no-visible-cursor-when-using-qxl-or-virtio

> For anyone who’s interested, this how I enabled the software cursor:

```
echo ''' Section "Device"
   Identifier "graphicsdriver"
   Option     "SWcursor" "on"
 EndSection''' | sudo tee /etc/X11/xorg.conf.d/vesa-swcursor.conf
 ```
