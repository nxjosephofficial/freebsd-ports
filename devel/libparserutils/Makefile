PORTNAME=	libparserutils
PORTVERSION=	0.2.5
CATEGORIES=	devel
MASTER_SITES=	http://download.netsurf-browser.org/libs/releases/
EXTRACT_SUFX=	-src.tar.gz

MAINTAINER=	nc@FreeBSD.org
COMMENT=	Lexer/parser utility functions for NetSurf
WWW=		https://www.netsurf-browser.org/projects/libparserutils/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	netsurf-buildsystem>=1.5:devel/netsurf-buildsystem

USES=		gmake iconv localbase pkgconfig
USE_LDCONFIG=	yes

MAKE_ENV=	BUILD_CC="${CC}" COMPONENT_TYPE="lib-shared"
LDFLAGS+=	${ICONV_LIB}

PLIST_SUB=	VERSION=${PORTVERSION}

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/libparserutils.so

.include <bsd.port.mk>
