include $(TOPDIR)/rules.mk

PKG_NAME:=python3-speedtest-cli
PKG_VERSION:=2.1.2
PKG_RELEASE:=1

PKG_SOURCE:=speedtest-cli-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://pypi.python.org/packages/source/s/speedtest-cli/
PKG_HASH:=cf1d386222f94c324e3125ba9a0d187e46d4a13dca08c023bdb9a23096be2e54

PKG_BUILD_DIR:=$(BUILD_DIR)/speedtest-cli-$(PKG_VERSION)

PKG_MAINTAINER:=Jaymin Patel <jem.patel@gmail.com>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-speedtest-cli
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Command line interface for testing internet bandwidth using speedtest.net
  URL:=https://github.com/sivel/speedtest-cli
  DEPENDS:=+python3-light +python3-xml +python3-email \
	  +python3-urllib +python3-codecs +python3-openssl
  VARIANT:=python3
endef

define Package/python3-speedtest-cli/description
  Command line interface for testing internet bandwidth using speedtest.net
endef

$(eval $(call Py3Package,python3-speedtest-cli))
$(eval $(call BuildPackage,python3-speedtest-cli))
$(eval $(call BuildPackage,python3-speedtest-cli-src))
