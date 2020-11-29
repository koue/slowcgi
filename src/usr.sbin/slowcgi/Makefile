#	$OpenBSD: Makefile,v 1.2 2014/12/05 20:02:41 florian Exp $

LOCALBASE?=	/usr/local
BINDIR?=	${LOCALBASE}/sbin
MANDIR?=	${LOCALBASE}/man/man
PROG=		slowcgi
SRCS=		slowcgi.c getdtablecount.c
CFLAGS+=	-Wall
CFLAGS+=	-Wstrict-prototypes -Wmissing-prototypes
CFLAGS+=	-Wmissing-declarations
CFLAGS+=	-Wshadow -Wpointer-arith -Wcast-qual
CFLAGS+=	-Wsign-compare
CFLAGS+=	-I${.CURDIR} \
		-I${.CURDIR}/../../../libevent/src/lib/libevent
CFLAGS+=	-D__dead=''
LDFLAGS+=	-L${.CURDIR}/../../../libevent/src/lib/libevent
LDADD=		-levent -lprocstat
DPADD=		${LIBEVENT}
MAN=		slowcgi.8
.include <bsd.prog.mk>
