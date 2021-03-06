#
# Copyright (C) Alexandru Ardelean <ardeleanalex@gmail.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=pymysql
PKG_VERSION:=0.9.3
PKG_RELEASE:=2

PKG_SOURCE:=PyMySQL-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://files.pythonhosted.org/packages/source/P/PyMySQL
PKG_HASH:=d8c059dcd81dedb85a9f034d5e22dcb4442c0b201908bede99e306d65ea7c8e7
PKG_BUILD_DIR:=$(BUILD_DIR)/PyMySQL-$(PKG_VERSION)

PKG_MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_CONFIG_DEPENDS:=CONFIG_PYTHON3_PYMYSQL_SHA_PASSWORD_SUPPORT

include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-pymysql
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Pure Python MySQL Client
  URL:=https://pymysql.readthedocs.io/
  DEPENDS:=+python3 +PYTHON3_PYMYSQL_SHA_PASSWORD_SUPPORT:python3-cryptography
  VARIANT:=python3
endef

define Package/python3-pymysql/config
  source "$(SOURCE)/Config.in"
endef

define Package/python3-pymysql/description
  This package contains a pure-Python MySQL client library, based on PEP 249.
endef

$(eval $(call Py3Package,python3-pymysql))
$(eval $(call BuildPackage,python3-pymysql))
$(eval $(call BuildPackage,python3-pymysql-src))
