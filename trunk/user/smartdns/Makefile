include $(ROOTDIR)/rules.mk

PKG_NAME:=smartdns
PKG_VERSION:=1.2023.41

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://www.github.com/pymumu/smartdns.git
PKG_SOURCE_VERSION:=b43601da65f6215080bac3ebbef63a27201de44b
PKG_MIRROR_HASH:=skip
include $(INCLUDE_DIR)/package.mk

$(eval $(call BuildPackage,smartdns))

romfs:
	$(INSTALL_DIR) $(ROMFSDIR)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/smartdns $(ROMFSDIR)/usr/bin/smartdns
	$(INSTALL_BIN) ./smartdns.sh $(ROMFSDIR)/usr/bin/smartdns.sh
	$(INSTALL_DIR) $(ROMFSDIR)/etc_ro/smartdns
	$(INSTALL_DATA) ./conf/*.conf $(ROMFSDIR)/etc_ro/smartdns/
	$(INSTALL_DATA) ./conf/*.txt $(ROMFSDIR)/etc_ro/smartdns/
