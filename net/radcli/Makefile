PORTNAME=	radcli
PORTVERSION=	1.3.1
MASTER_SITES=	https://github.com/radcli/radcli/releases/download/${PORTVERSION}/
CATEGORIES=	net

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Simple RADIUS client library
WWW=		https://radcli.github.io/radcli/ \
		https://github.com/radcli/radcli

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/COPYRIGHT

LIB_DEPENDS=	libgnutls.so:security/gnutls \
		libnettle.so:security/nettle

USES=		libtool pathfix pkgconfig

GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
INSTALL_TARGET=	install-strip
USE_LDCONFIG=	yes

post-install:
.for file in radiusclient.conf radiusclient-tls.conf servers servers-tls
	${INSTALL_DATA} ${WRKSRC}/etc/${file} ${STAGEDIR}${PREFIX}/etc/radcli/${file}.sample
.endfor

.include <bsd.port.mk>
