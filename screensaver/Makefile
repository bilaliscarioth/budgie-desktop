COMMENT =	budgie screensaver, screen saver and locker
DISTNAME =	budgie-screensaver-${BUDGIE_VERSION}

BUDGIE_VERSION =	5.1.0

CATEGORIES=	x11

MAINTAINER=	Bilal Emohmadian <bilal@iscarioth.org>

GH_ACCOUNT = bilaliscarioth
GH_PROJECT = budgie-screensaver
GH_COMMIT = a87bc18b24b0e9e5df4634846dc3c624cc96f88e

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
WANTLIB += Xxf86vm c cairo dbus-1 gdk-3 gdk_pixbuf-2.0 gio-2.0
WANTLIB += gobject-2.0 gtk-3

COMPILER =	base-clang

CFLAGS +=	-I${LOCALBASE}/include/

.include <bsd.port.mk>
