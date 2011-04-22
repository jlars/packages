
include $(TOPDIR)/rules.mk

PKG_NAME:=perl-crypt-openssl-rsa
PKG_VERSION:=0.26
PKG_RELEASE:=1
PKG_MD5SUM:=baf875f01ee39b88335b8f0962fe4bbc

PKG_SOURCE_URL:=http://search.cpan.org/CPAN/authors/id/I/IR/IROBERTS
PKG_SOURCE:=Crypt-OpenSSL-RSA-$(PKG_VERSION).tar.gz

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Crypt-OpenSSL-RSA-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-crypt-openssl-rsa
SUBMENU:=Perl
SECTION:=lang
CATEGORY:=Languages
TITLE:=HTTP style message
URL:=http://search.cpan.org/dist/Crypt-OpenSSL-RSA/
DEPENDS:=perl +libopenssl
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-crypt-openssl-rsa/install
$(call perlmod/Install,$(1),Crypt auto/Crypt)
endef


$(eval $(call BuildPackage,perl-crypt-openssl-rsa))
