# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

BOARD:=rockchip
BOARDNAME:=Rockchip
FEATURES:=ext4 audio usb usbgadget display gpio fpu pci pcie rootfs-part boot-part squashfs
SUBTARGETS:=armv8

KERNEL_PATCHVER=6.1
KERNEL_TESTING_PATCHVER=5.4

define Target/Description
	Build firmware image for Rockchip SoC devices.
endef

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES += uboot-envtools partx-utils resize2fs e2fsprogs mkf2fs kmod-gpio-button-hotplug kmod-usb-dwc2 kmod-usb3 kmod-usb-dwc3 \
		    automount autocore-arm autosamba fdisk luci-app-cpufreq cfdisk e2fsprogs ethtool haveged htop luci-app-diskman kmod-usb2-pci \
		    wpad-wolfssl libwolfssl-benchmark usb-modeswitch usbutils luci-app-zerotier luci-app-ttyd usb-modeswitch pciutils

KERNELNAME:=Image dtbs

$(eval $(call BuildTarget))
