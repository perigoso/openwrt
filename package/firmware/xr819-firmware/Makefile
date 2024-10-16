#
# Copyright (C) 2024 CZ.NIC z.s.p.o. (http://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=xr819-firmware
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/perigoso/xr819-firmware.git
PKG_SOURCE_DATE:=2024-10-16
PKG_SOURCE_VERSION:=208edb26f2c4b43958482b469698af274da054ee
# PKG_MIRROR_HASH:=

include $(INCLUDE_DIR)/package.mk

define Package/xr819-firmware
  SECTION:=firmware
  CATEGORY:=Firmware
  URL:=https://github.com/perigoso/xr819-firmware
  TITLE:=xr819 firmware
endef

define Package/xr819-firmware/description
Allwinner XR819 SDIO Wi-Fi chip firmware.
endef

define Build/Compile
	true
endef

define Package/xr819-firmware/install
	$(INSTALL_DIR) $(1)/lib/firmware/xr819/
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/*.bin $(1)/lib/firmware/xr819/
endef

$(eval $(call BuildPackage,xr819-firmware))
