PORTNAME=	KVIrc
DISTVERSION=	5.0.0-102
DISTVERSIONSUFFIX=	-geb3fdd6b1
PORTREVISION=	5
CATEGORIES=	irc kde

MAINTAINER=	kde@FreeBSD.org
COMMENT=	IRC client for KDE
WWW=		http://www.kvirc.net

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/doc/ABOUT-LICENSE

LIB_DEPENDS=	libaudiofile.so:audio/libaudiofile \
		libenchant.so:textproc/enchant

USES=		cmake compiler:c++11-lang cpe desktop-file-utils gettext gnome \
		kde:5 perl5 pkgconfig python qt:5 ssl tar:bzip2 xorg
USE_GNOME=	glib20
USE_PERL5=	run build
USE_KDE=	auth codecs config configwidgets coreaddons i18n notifications \
		phonon service widgetsaddons windowsystem xmlgui \
		ecm:build
USE_QT=		core dbus gui multimedia network printsupport sql svg \
		widgets x11extras xml \
		buildtools:build qmake:build
USE_XORG=	ice sm x11 xext xrender xscrnsaver
USE_LDCONFIG=	yes
USE_GITHUB=	yes

CMAKE_ARGS=	-DMANDIR_PREFIX:STRING=share/man

PLIST_SUB=	VER=5.0

.include <bsd.port.mk>
