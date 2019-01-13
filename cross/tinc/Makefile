PKG_NAME = tinc
PKG_VERS = 1.0.35
PKG_EXT = tar.gz
PKG_DIST_NAME = release-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/gsliepen/tinc/archive
PKG_DIR = $(PKG_NAME)-release-$(PKG_VERS)

DEPENDS = cross/zlib cross/lzo cross/openssl

HOMEPAGE = http://www.tinc-vpn.org
COMMENT  = A VPN daemon that uses tunnelling and encryption
LICENSE  = GPLv2

GNU_CONFIGURE = 1
PRE_CONFIGURE_TARGET = myPreConfigure

CONFIGURE_ARGS =

include ../../mk/spksrc.cross-cc.mk

.PHONY: myPreConfigure
myPreConfigure:
	$(RUN) autoreconf -i
