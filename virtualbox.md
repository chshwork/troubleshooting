### Shrink dynamically allocated disk
1. In a temporary or test VM, install zerofree (AUR)
2. Mount target disk as read-only (`mount -r`) in temp vm
   * Add disk using virtualbox > settings > storage
   * __NOTE: make sure that you are booted into the correct disk before zerofree__
   * If vbox won't boot into the correct disk, try switching SATA ports
4. `zerofree -v /dev/sdb2`
5. On host machine: `VBoxManage modifyhd /path/to/VDI/VM.vdi --compact`
### Windows 11 randomly freezes
- Solution: in VM settings, go to Display > Screen and change graphics controller to VBoxVGA
### Shared clipboard stops working 
- Description: Bidirectional clipboard stops working, guest -> host broken
- Solution: Kill the guest clipboard `VBoxClient --clipboard` and run it again
