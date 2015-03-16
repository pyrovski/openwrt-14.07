#
# Copyright (C) 2006-2012 OpenWrt.org
# Copyright 2010 Vertical Communications
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ceph
#PKG_VERSION:=giant
PKG_SOURCE_VERSION:=938e03630e075af03780da139ae879b5b0377734
PKG_RELEASE=$(PKG_SOURCE_VERSION)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_SOURCE_VERSION).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=git://github.com/ceph/ceph.git
PKG_SOURCE_PROTO:=git
PKG_FIXUP:=autoreconf

#https://github.com/ceph/ceph/archive/giant.zip
#PKG_SOURCE:=$(PKG_NAME)/archive/$(PKG_VERSION).zip

PKG_MAINTAINER:=Peter Bailey <peter.eldridge.bailey@gmail.com>

PKG_BUILD_DEPENDS:=util-linux
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/autotools.mk

define Package/ceph/Default
  URL:=https://github.com/ceph/ceph/
  SUBMENU:=Filesystem
endef

define Package/ceph
$(call Package/ceph/Default)
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Ceph distributed parallel filesystem
# +libblkid +libuuid +libudev +libkeyutils +libleveldb +libsepol1 +libsnappy +libunwind +python +xfslibs + libs3 +libs3-2 +libbsd +libedit +libfcgi +libfuse +libgoogle-perftools +libhamcrest-java +libselinux1 +libaio +libatomic-ops +libboost... +libnss3 +libnspr4
  DEPENDS:=+libblkid +libuuid +udev BROKEN
endef

define Package/ceph/description
  ceph
endef

define Package/ceph/install
	echo "install?"
endef

$(eval $(call BuildPackage,ceph))
