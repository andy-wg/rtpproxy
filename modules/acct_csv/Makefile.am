include $(top_srcdir)/m4/memdeb.ami
include $(top_srcdir)/m4/ccflags.ami

pkglib_LTLIBRARIES = rtpp_acct_csv.la rtpp_acct_csv_debug.la

rtpp_acct_csv_la_SOURCES = rtpp_acct_csv.c
rtpp_acct_csv_la_LDFLAGS = -avoid-version -module -shared -export-dynamic
rtpp_acct_csv_la_CPPFLAGS= -D_BSD_SOURCE

rtpp_acct_csv_debug_la_SOURCES = ${rtpp_acct_csv_la_SOURCES}
rtpp_acct_csv_debug_la_LIBADD = $(RTPP_MEMDEB_LDADD)
rtpp_acct_csv_debug_la_LDFLAGS=${rtpp_acct_csv_la_LDFLAGS}
rtpp_acct_csv_debug_la_CPPFLAGS=$(rtpp_acct_csv_la_CPPFLAGS) -DRTPP_DEBUG \
 $(RTPP_MEMDEB_CPPFLAGS) -DMEMDEB_APP="acct_csv"
rtpp_acct_csv_debug_la_CFLAGS=$(RTPP_MEMDEB_CFLAGS)

DEFS=	$(CC_WFLAGS) @DEFS@
