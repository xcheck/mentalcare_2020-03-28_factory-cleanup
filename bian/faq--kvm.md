# KVM kernel-based virtual machine
### requirements

+ ***cpu virt <sup>technology</sup> by intel…***

```
cat /etc/os-rlease; dmesg | grep -i virt; egrp '(vmx|svm)'
```


+ ***kernel-based modul kvm***

$ lsmod | grep kvm _« (Debian9)_

```
kvm_intel             192512  0
kvm                   589824  1 kvm_intel
irqbypass              16384  1 kvm
```


### kvm server

+ ***qemu-kvm <sup>exec qemu-system-x86_64 -enable-kvm "$@"</sup>***

```
apt install qemu [qemu-kvm] virt-manager
```


+ ***spice # client (remote?): VM-Video: QXL (2D) new VirtIO (3D) rendering <sup>ob¬ing</sup>***  
+ ***spice # client (guest?): video screen resizing <sup>ob¬ing</sup>***

```
apt install spice-client-gtk
```
```
apt install spice-vdagent
```


+ ***groupmod   # /etc/group « add user***

```
pi:x:1000:libvirt-qemu
libvirt:x:128:pi
libvirt-qemu:x:64055:libvirt-qemu,pi
```


### audio w/o-pa but.spice

+ ***spice requirement:***

host input audio device (figure HDMI/DP dues input) pegel independent  
USB audio device or any LINE-IN plug -- spice quick and dirty ,vnc otherwise  
or ALSA virtual device .. "snd-aloop snd-dummy modprobe" ... /etc/modules  
or "pacmd load-module module-virtual-source source_name=loop_source uplink_sink=loop_sink"