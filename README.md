# wiper
Automatic USB storage device wiper

This tool, will be started as system boots up and then Automatically will detect any USB storage device inserted and then wipes it out with random data using `dd` command

### prerequisites
- Ubuntu-based OS
- zenity
- xterm
- python and udev package for it

### Installation
1. copy `usb_detect.service` to `/lib/systemd/system/usb_detect.service`
2. Edit `User`, `ExecStart`, and `Environment` according to your configs
3. copy other two scripts to your Desktop
4. 
```bash
sudo systemctl enable usb_detect.service --now
sudo systemctl daemon-reload
sudo systemctl start usb_detect.service
sudo shutdown -r now
```
