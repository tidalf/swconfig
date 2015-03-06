dnl Skyld AV

dnl Initialization
AC_INIT([swconfig], [0.1], [xypron.glpk@gmx.de])
AM_INIT_AUTOMAKE([-Wall -Werror foreign])

dnl Archiver support.
AM_PROG_AR

dnl Enhanced libtool support.
LT_INIT

dnl Compiler check
AC_PROG_CC
AC_CHECK_PROG([have_cc],[$CC],[yes],[no])
if test [$have_cc] != [yes]; then
  AC_MSG_ERROR([$CC is missing])
fi

dnl Configure macros
AC_CONFIG_MACRO_DIR([m4])

dnl Load pkg.m4
PKG_PROG_PKG_CONFIG

PKG_CHECK_MODULES([SWCONFIG], [libnl-3.0, libnl-genl-3.0])

AC_MSG_NOTICE([CFLAGS = $CFLAGS])
AC_MSG_NOTICE([LDFLAGS  = $LDFLAGS])

dnl Makefiles
AC_CONFIG_FILES([
  Makefile
  src/Makefile
  ])

dnl Generate files
AC_OUTPUT
