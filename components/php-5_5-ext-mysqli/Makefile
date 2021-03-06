#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2013, EveryCity Ltd. All rights reserved.
#
include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		php
COMPONENT_VERSION=      5.5.24
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= sha256:43e6b83fe8151f8d2062ca4da915312fc92e47789801049231c705a8b29b05bc
COMPONENT_ARCHIVE_URL=	http://ru2.php.net/get/$(COMPONENT_ARCHIVE)/from/this/mirror

include ../../make-rules/prep.mk
include ../../make-rules/configure.mk
include ../../make-rules/ips.mk

PHP_PREFIX=/usr/php/5.5
PHP_SYSCONFDIR=/etc/php/5.5
PHP_DATADIR=/var/php/5.5

CONFIGURE_OPTIONS	=	--prefix=$(PHP_PREFIX)
CONFIGURE_OPTIONS.32	=	--bindir=$(PHP_PREFIX)/bin
CONFIGURE_OPTIONS.64	=	--bindir=$(PHP_PREFIX)/bin/$(MACH64)
CONFIGURE_OPTIONS.32  +=	--sbindir=$(PHP_PREFIX)/bin
CONFIGURE_OPTIONS.64  +=	--sbindir=$(PHP_PREFIX)/bin/$(MACH64)
CONFIGURE_OPTIONS.32  +=	--libdir=$(PHP_PREFIX)/lib
CONFIGURE_OPTIONS.64  +=	--libdir=$(PHP_PREFIX)/lib/$(MACH64)
CONFIGURE_OPTIONS.32  +=	--libexecdir=$(PHP_PREFIX)/libexec
CONFIGURE_OPTIONS.64  +=	--libexecdir=$(PHP_PREFIX)/libexec/$(MACH64)
CONFIGURE_OPTIONS     +=	--includedir=$(PHP_PREFIX)/include
CONFIGURE_OPTIONS     +=	--sysconfdir=$(PHP_SYSCONFDIR)
CONFIGURE_OPTIONS     +=	--datadir=$(PHP_DATADIR)
CONFIGURE_OPTIONS     +=	--mandir=$(PHP_PREFIX)/share/man

CONFIGURE_OPTIONS.64  +=	--build=x86_64-pc-solaris2.10
CONFIGURE_OPTIONS.32  +=	--with-php-config=$(PHP_PREFIX)/bin/php-config
CONFIGURE_OPTIONS.64  +=	--with-php-config=$(PHP_PREFIX)/bin/$(MACH64)/php-config
CONFIGURE_OPTIONS.32  +=	--with-mysqli=/usr/mariadb/5.5/bin/mysql_config
CONFIGURE_OPTIONS.64  +=	--with-mysqli=/usr/mariadb/5.5/bin/$(MACH64)/mysql_config

CONFIGURE_OPTIONS     +=	$(CONFIGURE_OPTIONS.$(BITS))

LDFLAGS.32            +=        -L/usr/mariadb/5.5/lib -R/usr/mariadb/5.5/lib
LDFLAGS.64            +=        -L/usr/mariadb/5.5/lib/$(MACH64) -R/usr/mariadb/5.5/lib/$(MACH64)

CFLAGS                  =       $(CC_BITS) -D_POSIX_PTHREAD_SEMANTICS
CFLAGS                  +=       -I/usr/mariadb/5.5/include
CPPFLAGS                +=      -I/usr/mariadb/5.5/include
LDFLAGS                 +=      $(LDFLAGS.$(BITS))

CONFIGURE_SCRIPT       =	$(@D)/configure

COMPONENT_PRE_CONFIGURE_ACTION	=	cp -R $(SOURCE_DIR)/ext/mysqli/* $(@D) ; \
	$(MKDIR) $(@D)/ext ; cp -R $(SOURCE_DIR)/ext/mysqlnd $(@D)/ext ; cd $(@D) ; $(PHP_PREFIX)/bin/phpize
COMPONENT_INSTALL_ARGS		+=	INSTALL_ROOT=$(PROTO_DIR)

build:		$(BUILD_32_and_64)

install:	$(INSTALL_32_and_64)
