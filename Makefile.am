# ind/Makefile.am

AUTOMAKE_OPTIONS = foreign

bin_PROGRAMS = ind
man_MANS = ind.1
ind_SOURCES = ind.c portable.c pty_solaris.c pty_socketpair.c openpty_getpty.c

mrproper: maintainer-clean
	rm -f aclocal.m4 configure.scan depcomp missing install-sh config.h.in
	rm -f Makefile.in configure autoscan*.log

doc:
	yodl2man -o ind.1 ind.yodl

check:
	mkdir -p testsuite/logs
	runtest
