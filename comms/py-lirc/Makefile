# Created by: Lewis Thompson (purple@lewiz.net)
# $FreeBSD$

PORTNAME=	lirc
PORTVERSION=	0.0.5
PORTREVISION=	4
CATEGORIES=	comms python
MASTER_SITES=	SF/py${PORTNAME}/py${PORTNAME}/${PORTVERSION}
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}
DISTNAME=	pylirc-${PORTVERSION}

MAINTAINER=	lewiz@compsoc.man.ac.uk
COMMENT=	Lirc support library for Python

DEPRECATED=	No longer maintained and not compatible with Python 3
EXPIRATION_DATE=	2021-04-15

LIB_DEPENDS=	liblirc_client.so:comms/lirc

CFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib

PLIST_FILES=	%%PYTHON_SITELIBDIR%%/pylircmodule.so

USES=			python:3.6+
USE_PYTHON=		distutils pythonprefix
PYDISTUTILS_PKGNAME=	pylirc

.include <bsd.port.mk>
