MAINTAINERCLEANFILES = Makefile.in aclocal.m4 configure depcomp \
		       config.guess config.sub missing install-sh \
		       ltmain.sh compile config.h.in config.h.in~ \
		       autoscan.log configure.scan test-driver

AUTOMAKE_OPTIONS = foreign

ACLOCAL_AMFLAGS = -I m4

noinst_PROGRAMS = hello_world

hello_world_SOURCES = main.c

check_PROGRAMS = hello_world

TESTS = $(check_PROGRAMS)

VALGRIND = $(VALGRIND_EXEC) -q --error-exitcode=127

MEMCHECK = $(VALGRIND) --track-fds=yes --leak-check=full

check-memcheck: $(check_PROGRAMS)
if DO_MEMCHECK
	$(MAKE) check LOG_COMPILE="libtool --mode=execute $(MEMCHECK)"
else
	@echo valgrind not supported on this platform
endif

maintainer-clean-local:
	rm -rf m4
