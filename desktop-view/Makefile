COMMENT =		budgie desktop view, familiar and modern  desktop environnment
DISTNAME =		budgie-desktop-view-${VERSION}
CATEGORIES =	x11

MAINTAINER =	Bilal Emohmadian <bilal@iscarioth.org>
VERSION =		1.2.1

# Apache-2.0 license
PERMIT_PACKAGE=Yes

RUN_DEPENDS = lang/vala

LIB_DEPENDS = devel/gettext,-tools

MODULES= devel/meson

WANTLIB= glib-2.0 gtk-3

# Budgie repository
GH_ACCOUNT = BuddiesOfBudgie
GH_PROJECT =  budgie-desktop-view
GH_COMMIT = ca255e44644a91dc21cb0882778d413049063088

COMPILER = 		base-clang

.include <bsd.port.mk>
