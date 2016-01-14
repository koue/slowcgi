#	$OpenBSD: Makefile,v 1.2 2014/12/05 20:02:41 florian Exp $

LOCALBASE?=	/usr/local
PROG=	slowcgi
SRCS=	slowcgi.c getdtablecount.c
CFLAGS+= -Wall
CFLAGS+= -Wstrict-prototypes -Wmissing-prototypes
CFLAGS+= -Wmissing-declarations
CFLAGS+= -Wshadow -Wpointer-arith -Wcast-qual
CFLAGS+= -Wsign-compare
CFLAGS+=	-I${.CURDIR} \
		-I${LOCALBASE}/include \
		-L${LOCALBASE}/lib \
		-D__dead=''
LDADD=	-levent -lprocstat
DPADD=	${LIBEVENT}
MAN=	slowcgi.8
.include <bsd.prog.mk>
