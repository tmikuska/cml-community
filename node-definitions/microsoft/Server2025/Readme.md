# Microsoft Server 2025

This directory contains the following node definition:

- `win2025.yaml` - Microsoft Windows Server 2025 node definition

### Image Availability

VHD images can be downloaded from microsoft on a trial basis here:

- [Evaluation Center](https://www.microsoft.com/en-us/evalcenter)

Then the VHD image will have to be converted to a .qcow2 format. Linux qumu-img makes it easy.

For example:

```sh
qemu-img convert -f vpc -O qcow2 \
  26100.1742.amd64fre.ge_release_svc_refresh.240906-0331_server_serverdatacentereval_en-us.vhdx \
  26100.1742.amd64fre.ge_release_svc_refresh.240906-0331_server_serverdatacentereval_en-us.qcow2
```

### Notes

This node definition uses 16g of RAM and 4vcpu's. Anything less than that and it tends to become buggy.
