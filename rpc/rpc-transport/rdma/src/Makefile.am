# TODO : need to change transportdir

transport_LTLIBRARIES = rdma.la
transportdir = $(libdir)/glusterfs/$(PACKAGE_VERSION)/rpc-transport

rdma_la_LDFLAGS = -module -avoidversion

rdma_la_SOURCES = rdma.c name.c
rdma_la_LIBADD = $(top_builddir)/libglusterfs/src/libglusterfs.la     \
	-libverbs

noinst_HEADERS = rdma.h name.h
	-I$(top_srcdir)/libglusterfs/src -I$(top_srcdir)/rpc/rpc-lib/src/ \
	-I$(top_srcdir)/xlators/protocol/lib/src/ -shared -nostartfiles $(GF_CFLAGS)

AM_CFLAGS = -fPIC $(GF_CPPFLAGS) -Wall \
	-I$(top_srcdir)/libglusterfs/src -I$(top_srcdir)/rpc/rpc-lib/src/ \
	-I$(top_srcdir)/rpc/xdr/src -shared -nostartfiles $(GF_CFLAGS)

CLEANFILES = *~
