COMMENT =		budgie, desktop environment
DISTNAME =		budgie-desktop-${VERSION}
CATEGORIES =	x11

MAINTAINER =	Bilal Emohmadian <bilal@iscarioth.org>
VERSION =			10.7

CONFIGURE_ARGS = \
	-Dwith-bluetooth=false \
	-Dwith-libuuid-time-safe=false

#GPLv2
PERMIT_PACKAGE=Yes

LIB_DEPENDS= \
	devel/libinotify \
	devel/gettext,-tools \
	devel/libpeas 

MODULES= devel/meson

WANTLIB = X11 canberra  glib-2.0 gtk-3 gnome-desktop-3 gee-0.8 gdk-x11-2.0
WANTLIB += gio-2.0 gdk-3 uuid intl cairo gstreamer-1.0 X11 

# Budgie repository
DISTFILES = v${VERSION}.tar.gz
MASTER_SITES =	https://github.com/bilaliscarioth/budgie-desktop/archive/refs/tags/

COMPILER = 		base-clang
CONFIGURE_ENV = LDFLAGS="-L/usr/X11R6/lib/"

.include <bsd.port.mk>
