include $(TOPDIR)/rules.mk

PKG_NAME:=mptcpd
PKG_VERSION:=0.14
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/jeff277/mptcpd.git
PKG_SOURCE_VERSION:=0ee204d357042737daacd8affd586cca4fe059bb
PKG_MIRROR_HASH:=skip

PKG_LICENSE:=LGPL-2.1-or-later
PKG_MAINTAINER:=jeff277 <164035526@qq.com>

PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=1
PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/mptcpd
	SECTION:=net
	CATEGORY:=Network
	TITLE:=mptcpd MPTCP daemon
	URL:=https://github.com/multipath-tcp/mptcpd
	DEPENDS:=+ell
	USERID:=mptcpd=320:mptcpd=320
endef

define Package/mptcpd/description
	mptcpd is a daemon that serves as a userspace path manager for Multipath TCP (MPTCP).
endef

define Package/mptcpd/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/mptcpd $(1)/usr/sbin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/mptcpize $(1)/usr/sbin/
	$(INSTALL_DIR) $(1)/usr/lib
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/libmptcpd.la $(1)/usr/lib/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/libmptcpd.so $(1)/usr/lib/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/libmptcpd.so.3 $(1)/usr/lib/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/libmptcpd.so.3.0.0 $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/usr/lib/mptcpd
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpd/addr_adv.la $(1)/usr/lib/mptcpd/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpd/addr_adv.so $(1)/usr/lib/mptcpd/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpd/sspi.la $(1)/usr/lib/mptcpd/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpd/sspi.so $(1)/usr/lib/mptcpd/
	$(INSTALL_DIR) $(1)/usr/lib/mptcpize
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpize/libmptcpwrap.la $(1)/usr/lib/mptcpize/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpize/libmptcpwrap.so $(1)/usr/lib/mptcpize/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpize/libmptcpwrap.so.0 $(1)/usr/lib/mptcpize/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/mptcpize/libmptcpwrap.so.0.0.1 $(1)/usr/lib/mptcpize/
	$(INSTALL_DIR) $(1)/usr/lib/pkgconfig
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/mptcpd.pc $(1)/usr/lib/mptcpize/
	$(INSTALL_DIR) $(1)/etc/mptcpd
	$(INSTALL_CONF) $(PKG_INSTALL_DIR)/etc/mptcpd/mptcpd.conf $(1)/etc/mptcpd/
endef


$(eval $(call BuildPackage,mptcpd))

