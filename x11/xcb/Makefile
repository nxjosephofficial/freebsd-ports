PORTNAME=	xcb
PORTVERSION=	2.4
PORTREVISION=	4
CATEGORIES=	x11
MASTER_SITES=	http://oldhome.schmorp.de/marc/data/ \
		http://ftp.lyx.org/pub/pcg/marc/ \
		http://fossies.org/unix/misc/old/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Tool for managing x11 cut-buffers
WWW=		http://oldhome.schmorp.de/marc/xcb.html

LICENSE=	MIT

USES=		imake xorg
USE_XORG=	ice sm x11 xaw xext xmu xt

PLIST_FILES=	bin/xcb \
		lib/X11/app-defaults/Xcb \
		share/man/man1/xcb.1.gz

.include <bsd.port.mk>
