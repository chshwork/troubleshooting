### Guest additions won't start 
- `systemctl status vboxdrmclient` shows error `VBoxDRMClient: Fatal Error: Failed to request display change events, rc=VERR_INVALID_HANDLE`
- Run `sudo rcvboxadd setup`
- In this case it told me I didn't have lts kernel headers installed
### Dynamically allocated disk getting too large
1. In a temporary or test VM, install zerofree (AUR)
2. Mount target disk as read-only (`mount -r`) in temp vm
   * Add disk using virtualbox > settings > storage
   * __NOTE: make sure that you are booted into the correct disk before zerofree__
   * If vbox won't boot into the correct disk, try switching SATA ports
4. `zerofree -v /dev/sdb2`
5. On host machine: `VBoxManage modifyhd /path/to/VDI/VM.vdi --compact`
### Windows 11 randomly freezes
- in VM settings, go to Display > Screen and change graphics controller to VBoxVGA
### Shared clipboard stops working 
- Bidirectional clipboard stops working, guest -> host broken
- Kill the guest clipboard `VBoxClient --clipboard` and run it again
### Resizing window causes guest to freeze
- Linux guest freezes/blackscreens when trying to auto-resize on a wide screen
- Increase the Video Memory in Settings > Display > Screen
