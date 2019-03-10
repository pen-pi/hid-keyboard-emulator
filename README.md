# HID Creator Script

This script must be run once to create the fake hid device.   
Will ussualy load the device under `/dev/hidg0`.   
This scrupt must be run as `root`. 

# Executing at Boot
To execute this command at boot we can execute the script by invoking it inside of `/etc.rc.local`.   
This will execute at the end of single user mode, when entering multiuser mode (at runlevel change).   
We must make sure not to break the file and our program must `exit 0`.   


In order to do this we:
   - Copy or move `hid-penpi` to `/usr/bin/hid-penpi`
   - Add `/usr/bin/hid-penpi # libcomposite configuration` to `/etc.rc.local`
      - This must be added before the `exit 0` in `/etc.rc.local`


# Notes
   - Kernel modules of the form `g_*` must be unloaded before this script is ran
   - If necesary unload them, run the script and then reload them

