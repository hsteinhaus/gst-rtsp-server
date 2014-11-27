noinst_PROGRAMS = test-video test-ogg test-mp4 test-readme \
		  test-launch test-sdp test-uri test-auth \
		  test-multicast test-multicast2 test-appsrc

bin_PROGRAMS = tls
tls_SOURCES= tls.c

#INCLUDES = -I$(top_srcdir) -I$(srcdir)

AM_CFLAGS = $(GST_OBJ_CFLAGS)
LDADD = $(GST_OBJ_LIBS) $(GIO_LIBS)

if HAVE_LIBCGROUP
noinst_PROGRAMS += test-cgroups
LDADD += $(LIBCGROUP_LIBS)
endif


noinst_PROGRAMS += test-launch2

test-launch2$(EXEEXT):
	echo "Foobar!!!!" > /tmp/hello.txt
	gcc -o test-launch2 test-launch.c -I /usr/include/gstreamer-1.0 -I /usr/include/glib-2.0/ -I /usr/lib/arm-linux-gnueabihf/glib-2.0/include -L /usr/lib/arm-linux-gnueabihf/ -lglib-2.0 -lgstreamer-1.0 -lgobject-2.0 -lgstrtspserver-1.0
