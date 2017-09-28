MAINTAINERCLEANFILES = Makefile.in aclocal.m4 configure depcomp \
		       config.guess config.sub missing install-sh \
		       ltmain.sh compile config.h.in config.h.in~ \
		       autoscan.log configure.scan test-driver

AUTOMAKE_OPTIONS = foreign

ACLOCAL_AMFLAGS = -I m4

noinst_PROGRAMS = hello_world

hello_world_SOURCES = main.c

maintainer-clean-local:
	rm -rf m4
