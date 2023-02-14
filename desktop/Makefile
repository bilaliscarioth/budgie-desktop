COMMENT =	budgie, desktop environment
DISTNAME =	budgie-desktop-${VERSION}
CATEGORIES =	x11

MAINTAINER =	Bilal Emohmadian <bilal@iscarioth.org>
VERSION =	10.7

GH_ACCOUNT = bilaliscarioth
GH_PROJECT = budgie-desktop
GH_COMMIT = 70424bcee090ebe034fd76cb72d206a50bdd0b49


CONFIGURE_ARGS = \
	-Dwith-bluetooth=false \
	-Dwith-libuuid-time-safe=false

#GPLv2 / LGPLv2
PERMIT_PACKAGE=Yes

MODGNOME_TOOLS=	desktop-file-utils gtk-update-icon-cache

LIB_DEPENDS= \
	devel/gettext,-tools \
	devel/libpeas \
	devel/libinotify \
	graphics/gdk-pixbuf2 \
	devel/libwnck \
	devel/libgee \
	inputmethods/ibus 

RUN_DEPENDS = \
	lang/vala  \
	devel/desktop-file-utils \
	x11/gtk+3,-guic \
	devel/cmake \
	x11/gnome/desktop

SHARED_LIBS +=  budgie-appindexer         0.0 # 0.0
SHARED_LIBS +=  budgie-plugin             0.0 # 0.0
SHARED_LIBS +=  budgie-private            0.0 # 0.0
SHARED_LIBS +=  budgie-raven-plugin       0.0 # 0.0
SHARED_LIBS +=  budgietheme               0.0 # 0.0
SHARED_LIBS +=  raven                     0.0 # 0.0


WANTLIB += GL ICE SM X11 X11-xcb Xcomposite Xcursor Xdamage Xext Xfixes
WANTLIB += Xi Xinerama Xrandr Xrender Xss Xxf86vm atk-1.0 atk-bridge-2.0
WANTLIB += c cairo cairo-gobject dbus-1 dbus-glib-1 dconf drm epoxy
WANTLIB += expat ffi fontconfig freetype fribidi gdk-3 gdk_pixbuf-2.0
WANTLIB += gio-2.0 glapi glib-2.0 gmodule-2.0 gobject-2.0 graphite2
WANTLIB += gthread-2.0 gtk-3 harfbuzz iconv intl lzma m notify pango-1.0
WANTLIB += pangoft2-1.0 pcre2-8 pixman-1 png pthread startup-notification-1
WANTLIB += xcb xcb-dri2 xcb-dri3 xcb-glx xcb-present xcb-render xcb-shm
WANTLIB += xcb-sync xcb-util xcb-xfixes xkbfile xklavier xml2 xshmfence
WANTLIB += gee-0.8 girepository-1.0 ibus-1.0 peas-1.0
WANTLIB += z pangocairo-1.0 canberra 

MODULES= devel/meson \
	x11/gnome

COMPILER = base-clang
CFLAGS = -L/usr/X11R6/lib/


post-install:
	@mkdir -p ${PREFIX}/share/examples/budgie-desktop/xdg/autostart
	@mv ${WRKINST}/etc/xdg/autostart \
	${PREFIX}/share/examples/budgie-desktop/xdg/autostart

.include <bsd.port.mk>
