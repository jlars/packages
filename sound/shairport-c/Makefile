#
# Copyright (C) 2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=shairport-c
PKG_VERSION:=0.05
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
#PKG_SOURCE_URL:=git://github.com/albertz/shairport.git
PKG_SOURCE_URL:=git://github.com/Andywebs/shairport.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=17640f2ec1e1f7b3aeb4eb6e1795c0684370017c
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/shairport-c
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=Server for RAOP protocol
  URL:=http://mafipulation.org/
  DEPENDS:=+libopenssl +libao +avahi-daemon +avahi-utils
endef

define Package/shairport-c/description
  Shairport is server software that implements the RAOP protocol for
  playback of music streamed from a compatible remote client.
endef

define Package/shairport-c/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/{hairtunes,shairport} $(1)/usr/bin/
endef

$(eval $(call BuildPackage,shairport-c))
