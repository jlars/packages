#
# Copyright (C) 2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=shairport
PKG_VERSION:=0.05
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/albertz/shairport.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=d670169c522266d5ba448aba432508d8e1f402e5
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/shairport
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=Server for RAOP protocol
  URL:=http://mafipulation.org/
  DEPENDS:= +libopenssl +libao +avahi-daemon +avahi-utils +perl \
      +perl-crypt-openssl-rsa +perl-getopt-long \
      +perl-http-message +perl-uri \
      +perlbase-autoloader +perlbase-config +perlbase-cwd \
      +perlbase-digest +perlbase-dynaloader +perlbase-errno \
      +perlbase-essential +perlbase-fcntl +perlbase-feature \
      +perlbase-file +perlbase-findbin +perlbase-io \
      +perlbase-ipc +perlbase-mime +perlbase-posix \
      +perlbase-selectsaver +perlbase-socket +perlbase-symbol \
      +perlbase-tie +perlbase-xsloader
endef

define Package/shairport/description
  Shairport is server software that implements the RAOP protocol for
  playback of music streamed from a compatible remote client.
endef

define Package/shairport/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/{hairtunes,shairport.pl} $(1)/usr/bin/
endef

$(eval $(call BuildPackage,shairport))
