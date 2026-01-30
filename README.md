# device_xiaomi_spring-recovery

Recovery tree for this Xiaomi device
- Xiaomi Redmi _15_ 5G / _15R_ 5G / _POCO M7+_ 5G (codename: `spring`) (August 2025)

## Device specifications

Device                  | Redmi 15 5G / 15R 5G / POCO M7+ 5G
:-----------------------|:-------------------------------------
SoC                     | Qualcomm Snapdragon® 6s Gen 3 (SM6375-AC)
Board                   | `blair`
CPU                     | Octa-core (2x2.3 GHz Cortex-A78 & 6x2.0 GHz Cortex-A55)
GPU                     | Adreno 619
Memory                  | 4/6/8/12 GB RAM
Shipped Android Version | 15.0 (HyperOS 2)
Storage                 | 128/256/512 GB (UFS 2.2)
MicroSD                 | Yes (Hybrid Slot)
Battery                 | Non-removable Li-Po 7000 mAh
Dimensions              | 169.5 x 80.5 x 8.4 mm
Display                 | 6.9" FHD+ IPS LCD, 144Hz, 1080x2460

## Checklist
- [ ] ADB
- [ ] Decryption
- [ ] Touchscreen
- [ ] FastbootD
- [ ] Flashing
- [ ] MTP
- [ ] Sideload
- [ ] Backups
- [ ] Filesystems/Mounts
- [ ] Slot switch
- [ ] Haptics
- [ ] Flashlight
- [ ] Custom splash

## Notes
This device does not have a eSIM, meaning that instead of using Secure Element/StrongBox for decryption, 
TEE is used instead

```
vendor.gatekeeper.disable_spu=true
vendor.gatekeeper.is_security_level_spu=0
```

## How to build
This recovery tree was initially made for `spring`. For historical purposes,
build the `twrp_spring` target

```shell
lunch twrp_spring-ap2a-eng && mka adbd recoveryimage
```
