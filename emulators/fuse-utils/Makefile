PORTNAME=	fuse-utils
DISTVERSION=	1.4.3
PORTREVISION=	3
CATEGORIES=	emulators
MASTER_SITES=	SF/fuse-emulator/${PORTNAME}/${PORTVERSION}

MAINTAINER=	rene@FreeBSD.org
COMMENT=	Utilities from the Free Unix Spectrum Emulator
WWW=		https://fuse-emulator.sourceforge.net/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

LIB_DEPENDS=	libaudiofile.so:audio/libaudiofile \
		libgcrypt.so:security/libgcrypt \
		libpng.so:graphics/png \
		libspectrum.so:emulators/libspectrum

USES=		gettext gnome iconv jpeg pkgconfig
USE_GNOME=	glib20

GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
CONFIGURE_ARGS=	--with-libspectrum-prefix=${LOCALBASE} \
		--with-local-prefix=${LOCALBASE}

OPTIONS_DEFINE=	DOCS

post-install:
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	cd ${WRKSRC} && ${INSTALL_DATA} AUTHORS ChangeLog README ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
