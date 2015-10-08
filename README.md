# stuff
different configuration files

-- added apparmor config for skype

## Install Apparmor Debian :)

sudo apt-get install apparmor apparmor-profiles apparmor-utils

sudo perl -pi -e 's,GRUB_CMDLINE_LINUX="(.*)"$,GRUB_CMDLINE_LINUX="$1 apparmor=1 security=apparmor",' /etc/default/grub

sudo update-grub

 sudo reboot
