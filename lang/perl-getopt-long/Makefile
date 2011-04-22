
include $(TOPDIR)/rules.mk

PKG_NAME:=perl-getopt-long
PKG_VERSION:=2.38
PKG_RELEASE:=1
PKG_MD5SUM:=4d38c78300e79a7fde4700e88759c2b3

PKG_SOURCE_URL:=http://search.cpan.org/CPAN/authors/id/J/JV/JV
PKG_SOURCE:=Getopt-Long-$(PKG_VERSION).tar.gz

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Getopt-Long-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-getopt-long
SUBMENU:=Perl
SECTION:=lang
CATEGORY:=Languages
TITLE:=HTTP style message
URL:=http://search.cpan.org/dist/Getopt-Long/
DEPENDS:=perl
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-getopt-long/install
$(call perlmod/Install,$(1),newgetopt.pl Getopt)
endef


$(eval $(call BuildPackage,perl-getopt-long))
