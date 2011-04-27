
include $(TOPDIR)/rules.mk

PKG_NAME:=perl-io-socket-inet6
PKG_VERSION:=2.67
PKG_RELEASE:=1
PKG_MD5SUM:=228c12e74df686f78b09aee1139dc11c

PKG_SOURCE_URL:=http://search.cpan.org/CPAN/authors/id/S/SH/SHLOMIF
PKG_SOURCE:=IO-Socket-INET6-$(PKG_VERSION).tar.gz

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/IO-Socket-INET6-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-io-socket-inet6
SUBMENU:=Perl
SECTION:=lang
CATEGORY:=Languages
TITLE:=Object interface for AF_INET|AF_INET6 domain sockets
URL:=http://search.cpan.org/dist/IO-Socket-INET6-2.67/
DEPENDS:=perl
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-io-socket-inet6/install
$(call perlmod/Install,$(1),IO)
endef


$(eval $(call BuildPackage,perl-io-socket-inet6))
