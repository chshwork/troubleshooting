### Windows 11 randomly freezes
- Solution: in VM settings, go to Display > Screen and change graphics controller to VBoxVGA
### Shared clipboard stops working 
- Description: Bidirectional clipboard stops working, guest -> host broken
- Solution: Kill the guest clipboard `VBoxClient --clipboard` and run it again
