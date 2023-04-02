# SPDX-License-Identifier: GPL-2.0-only

# auto-detect subdirs
ifeq ($(CONFIG_ARCH_BENGAL), y)
include $(srctree)/techpack/camera/config/bengalcamera.conf
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera/config/bengalcameraconf.h
endif

ifdef CONFIG_SPECTRA_CAMERA_BENGAL
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/camera/include/uapi

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/camera/include/uapi \
                -I$(srctree)/techpack/camera/include
obj-y += drivers/
endif
