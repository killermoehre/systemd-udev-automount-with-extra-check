Example how to AV scan added USB devices on plug-in time.

# Why

Someone asked in #systemd on freenode.net how to do this.

# How

The device is mounted (`av-mount@.service`) and scanned (`av-scan@.service`). If the scan process fails, than the device is automatically unmounted (`av-umount@.service`).

# Future?

I don't know. Probably something with namespacing or access rights would be nice. Maybe tagging it in `udev` that it is in fact safe to mount to give the normal userspace control again.

Right now it can be really easy cheesed.
