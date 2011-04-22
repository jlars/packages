
include $(TOPDIR)/rules.mk

PKG_NAME:=perl-http-message
PKG_VERSION:=6.02
PKG_RELEASE:=1
PKG_MD5SUM:=a6b28e44f7b5e5573362f042d522a456

PKG_SOURCE_URL:=http://search.cpan.org/CPAN/authors/id/G/GA/GAAS
PKG_SOURCE:=HTTP-Message-$(PKG_VERSION).tar.gz

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/HTTP-Message-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-http-message
SUBMENU:=Perl
SECTION:=lang
CATEGORY:=Languages
TITLE:=HTTP style message
URL:=http://search.cpan.org/dist/HTTP-Message/
DEPENDS:=perl
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-http-message/install
$(call perlmod/Install,$(1),HTTP)
endef


$(eval $(call BuildPackage,perl-http-message))
