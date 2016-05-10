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

COMPONENT_NAME=		findlib
COMPONENT_VERSION=	1.5.5
COMPONENT_PROJECT_URL=	http://projects.camlcity.org/projects/findlib.html
COMPONENT_FMRI=		library/ocaml/findlib
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	\
	sha256:aafaba4f7453c38347ff5269c6fd4f4c243ae2bceeeb5e10b9dab89329905946
COMPONENT_ARCHIVE_URL=	http://download.camlcity.org/download/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	MIT
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=	Findlib is a library manager for Objective Caml.
COMPONENT_CLASSIFICATION=Development/Other Languages

CONFIGURE_DEFAULT_DIRS=no

include ../../../make-rules/prep.mk
include ../../../make-rules/configure.mk
include ../../../make-rules/ips.mk

CONFIGURE_OPTIONS  = -bindir $(CONFIGURE_PREFIX)/bin
CONFIGURE_OPTIONS += -mandir $(CONFIGURE_PREFIX)/share/man
CONFIGURE_OPTIONS += -sitelib $(CONFIGURE_PREFIX)/lib/ocaml/site-lib
CONFIGURE_OPTIONS += -config /etc/findlib.conf

COMPONENT_PRE_CONFIGURE_ACTION=$(CLONEY) $(SOURCE_DIR) $(@D)

COMPONENT_BUILD_TARGETS=all opt

COMPONENT_INSTALL_ENV += prefix=$(PROTO_DIR)

build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(TEST_32)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS) ocaml

include ../../../make-rules/depend.mk
