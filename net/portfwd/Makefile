PORTNAME=	portfwd
PORTVERSION=	0.29
PORTREVISION=	2
CATEGORIES=	net
MASTER_SITES=	SF

MAINTAINER=	ale@FreeBSD.org
COMMENT=	Port Forwarding Daemon
WWW=		https://portfwd.sourceforge.net/

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

OPTIONS_DEFINE=	DOCS EXAMPLES

GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=	${PREFIX}/share
USES=		autoreconf gmake
USE_RC_SUBR=	${PORTNAME}

post-patch:
	@${REINPLACE_CMD} -e "s|-Wall -ggdb -O3|${CFLAGS}|g" \
		${WRKSRC}/src/Makefile.am
	@${REINPLACE_CMD} -e "s|-Wall -g -O3|${CFLAGS}|g" \
		${WRKSRC}/tools/Makefile.am
	@${REINPLACE_CMD} -e "s|register ||g" \
		${WRKSRC}/src/lexconf.c ${WRKSRC}/src/yconf.c
	@${TOUCH} ${WRKSRC}/* ${WRKSRC}/*/*

post-install:
	${INSTALL_SCRIPT} ${WRKDIR}/${PORTNAME} ${STAGEDIR}${PREFIX}/etc/rc.d

post-install-EXAMPLES-on:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${WRKSRC}/cfg/*.cfg ${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
