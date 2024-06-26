PORTNAME=	freenit
DISTVERSION=	0.2.31
CATEGORIES=	www devel python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	meka@tilda.center
COMMENT=	REST API framework based on Flask-Smorest
WWW=		https://github.com/freenit-framework/backend

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

BROKEN=		py39-pydantic-1.10.14,1 conflicts with py39-pydantic2-2.5.3 (installs files into the same place)

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}email-validator>=0:mail/py-email-validator@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}fastapi>=0:www/py-fastapi@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}passlib>=0:security/py-passlib@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pyjwt>=0:www/py-pyjwt@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}uvicorn>=0:www/py-uvicorn@${PY_FLAVOR}
TEST_DEPENDS=	${PYTHON_PKGNAMEPREFIX}httpx>=0:www/py-httpx@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pytest-asyncio>=0:devel/py-pytest-asyncio@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pytest-factoryboy>=0:devel/py-pytest-factoryboy@${PY_FLAVOR}

USES=		python
USE_PYTHON=	autoplist concurrent distutils pytest
USE_RC_SUBR=	freenit

TEST_ENV=	PYTHONPATH=${WRKSRC}/src
TEST_ARGS=	--ignore=${PORTNAME}/project
NO_ARCH=	yes
SUB_LIST=	PYTHON_VER=${PYTHON_VER}

OPTIONS_DEFINE=		ORMAR
OPTIONS_DEFAULT=	ORMAR

ORMAR_DESC=		Support for SQL databases using Ormar
ORMAR_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}alembic>=0:databases/py-alembic@${PY_FLAVOR} \
			${PYTHON_PKGNAMEPREFIX}ormar>0:databases/py-ormar@${PY_FLAVOR}

.include <bsd.port.mk>
