COMMENT =	budgie screensaver, screen saver and locker
DISTNAME =	budgie-screensaver-${BUDGIE_VERSION}

BUDGIE_VERSION =	5.1.0

CATEGORIES=	x11

MAINTAINER=	Bilal Emohmadian <bilal@iscarioth.org>

GH_ACCOUNT = bilaliscarioth
GH_PROJECT = budgie-screensaver
GH_COMMIT = e54d7e7be8d338c98927cf5d7fd52ec4edccfca4

# GNU GPLv2
PERMIT_PACKAGE=	Yes

LIB_DEPENDS = \
	devel/gettext,-tools \
	devel/gsettings-desktop-schemas

RUN_DEPENDS = \
	x11/gnome/libgnomekbd

CONFIGURE_ARGS = \
	-Dwith-systemd=false \
	-Dwith-bsd_auth=true

MODULES= devel/meson 

WANTLIB = X11 glib-2.0 gnome-desktop-3 dbus-glib-1 intl
WANLIB += gio-2.0

COMPILER =	base-clang

CFLAGS +=	-I${LOCALBASE}/include/

.include <bsd.port.mk>
