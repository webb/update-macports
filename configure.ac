# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([Update Macports],[0],[https://github.com/webb/update-macports/issues],[update-macports],[https://github.com/webb/update-macports/])

dnl if test "x$prefix" = "xNONE"
dnl then AC_MSG_ERROR([\$prefix is unset. Set with --prefix=\${install root directory}])
dnl fi

default_macports_root_dir=/opt/local
if test "x$macports_root_dir" = "x"
then echo "Variable macports_root_dir not set. Using default ($default_macports_root_dir)"
macports_root_dir=$default_macports_root_dir
fi

if test ! -d "$macports_root_dir"
then AC_MSG_ERROR([macports_root_dir $macports_root_dir is not an existing dir])
else AC_SUBST([macports_root_dir], [$macports_root_dir])
fi

# Checks for programs.
AC_PROG_INSTALL
AC_PROG_MKDIR_P
AC_PROG_SED

# only put critical programs required to build 'all' here.

AC_PATH_PROG(anacron,anacron)
test "x$anacron" = "x" && AC_MSG_ERROR([anacron not found])

AC_PATH_PROG(bash,bash)
test "x$bash" = "x" && AC_MSG_ERROR([bash not found])

AC_PATH_PROGS(m4,gm4 m4)
test "x$m4" = "x" && AC_MSG_ERROR([m4 not found])

AC_PATH_PROG(sudo,sudo)
test "x$sudo" = "x" && AC_MSG_ERROR([sudo not found])

AC_CONFIG_FILES([Makefile], [chmod 444 Makefile])
AC_SUBST([config_files],$ac_config_files)
AC_OUTPUT
