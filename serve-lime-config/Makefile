include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/package.mk

PKG_NAME:=serve-lime-config
PKG_VERSION=$(GIT_COMMIT_DATE)-$(GIT_COMMIT_TSTAMP)
GIT_COMMIT_DATE:=$(shell git log -n 1 --pretty=%ad --date=short . )
GIT_COMMIT_TSTAMP:=$(shell git log -n 1 --pretty=%at . )

define Package/$(PKG_NAME)
    TITLE:=$(PKG_NAME)
    CATEGORY:=LiMe
    MAINTAINER:=Nicolas Pace <nico@libre.ws>
    URL:=http://libremesh.org
    DEPENDS:=
endef

define Package/$(PKG_NAME)/description
    Exposes the network's config through uhttpd.
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
    $(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
