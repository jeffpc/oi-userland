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
# Copyright 2015 Josef 'Jeff' Sipek <jeffpc@josefsipek.net>
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		extlib
COMPONENT_VERSION=	1.5.3
COMPONENT_PROJECT_URL=	https://code.google.com/p/ocaml-extlib/
COMPONENT_FMRI=		library/ocaml/extlib
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	\
	sha256:c095eef4202a8614ff1474d4c08c50c32d6ca82d1015387785cf03d5913ec021
COMPONENT_ARCHIVE_URL=	http://ocaml-extlib.googlecode.com/files/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	LGPL2
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=	ExtLib is a standard library for the OCaml programming langage. 
COMPONENT_CLASSIFICATION=Development/Other Languages

CONFIGURE_DEFAULT_DIRS=no

include ../../../make-rules/prep.mk
include ../../../make-rules/justmake.mk
include ../../../make-rules/ips.mk

build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(TEST_32)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS) \
	runtime/ocaml library/ocaml/findlib

include ../../../make-rules/depend.mk
