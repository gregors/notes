## QEMU

### Create Image Ready for Installation

To create an image ready for installation, use the following command:

```bash
qemu-img create -f qcow2 Image.img 10G
```

### Launch Virtual Machine

#### For Linux:

```bash
qemu-system-x86_64 -cdrom ubuntu.iso -boot menu=on -drive file=Image.img -m 2G -accel kvm
```

#### For macOS:

```bash
qemu-system-x86_64 -cdrom ubuntu.iso -boot menu=on -drive file=Image.img -m 2G -accel hvf
```
