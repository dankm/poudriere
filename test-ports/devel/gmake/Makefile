# Created by: jkh
# $FreeBSD: head/devel/gmake/Makefile 418216 2016-07-08 11:24:18Z tijl $

PORTNAME=	gmake
PORTVERSION=	4.2.1
PORTREVISION=	1
CATEGORIES=	devel
MASTER_SITES=	GNU/make
DISTNAME=	make-${PORTVERSION}

# note: before committing to this port, contact portmgr to arrange for an
# experimental ports run.  Untested commits may be backed out at portmgr's
# discretion.
MAINTAINER=	tijl@FreeBSD.org
COMMENT=	GNU version of 'make' utility

LICENSE=	GPLv3
LICENSE_FILE=	${WRKSRC}/COPYING

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--program-prefix=g \
		--without-guile
# fmake does not like PO_DEPENDS_ON_POT being undefined
MAKE_ARGS=	PO_DEPENDS_ON_POT=

USES=		cpe tar:bzip2
CPE_VENDOR=	gnu

OPTIONS_DEFINE=	NLS
OPTIONS_SUB=	yes

NLS_USES=	gettext iconv
NLS_CONFIGURE_ON=	${ICONV_CONFIGURE_ARG} \
			--with-libintl-prefix=${LOCALBASE}
NLS_CONFIGURE_ENABLE=	nls

INFO=		make

.include <bsd.port.mk>
