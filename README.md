# HID Creator Script

This script must be run once to create the fake hid device.   
Will ussualy load the device under `/dev/hidg0`.   
This scrupt mus be run as `root`.   

# Note
   - Kernel modules of the form `g_*` must be unloaded before this script is ran
   - If necesary unload them, run the script and then reload them

