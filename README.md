# Apple MFi devices fast-charge support

Exports a `charge_type` for supported Apple MFi devices, so that those
devices can be made to either trickle charge (500mA), or draw much more
current, as explained in the “USB Power Capability Vendor Request” section
of the [Accessory Design Guidelines for Apple Devices](https://developer.apple.com/accessories/Accessory-Design-Guidelines.pdf).

Note that an [earlier version of the guidelines](https://usermanual.wiki/Document/MFiAccessoryHardwareSpecificationR9NoRestriction.875543417.pdf) had a slightly different “API”.

Both documents are also available in the docs/ subdirectory.

The driver is only available inside the kernel itself as at the time it was
written, significant changes to the core USB sub-system were needed to make
it work. The driver itself was merged at the same time as the supporting
changes and cannot work on older kernels.
