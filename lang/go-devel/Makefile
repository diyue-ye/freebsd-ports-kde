# Created by: Devon H. O'Dell <devon.odell@gmail.com>
# $FreeBSD$

PORTVERSION=	g20210216
# Always set PORTREVISION and PORTEPOCH explicitly as otherwise it is inherited from lang/go
PORTREVISION=	0
PORTEPOCH=	0
MASTER_SITES=	https://github.com/dmgk/go-bootstrap/releases/download/${BOOTSTRAP_TAG}/:bootstrap \
		LOCAL/dmgk:bootstrap
PKGNAMESUFFIX=	-devel
DISTFILES=	go-${OPSYS:tl}-${GOARCH_${ARCH}}${GOARM_${ARCH}}-${BOOTSTRAP_TAG}.tar.xz:bootstrap

COMMENT=	Go programming language (development version)

USE_GITHUB=	yes
GH_ACCOUNT=	golang
GH_TAGNAME=	f21be2fdc6f1becdbed1592ea0b245cdeedc5ac8

CONFLICTS_INSTALL=	go

MASTERDIR=	${.CURDIR}/../go
PATCHDIR=	${.CURDIR}/files
DISTINFO_FILE=	${.CURDIR}/distinfo

post-extract:
	@[ -f ${WRKSRC}/VERSION ] || ${ECHO_CMD} "devel +${GH_TAGNAME}" > ${WRKSRC}/VERSION

.include "${MASTERDIR}/Makefile"
