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

COMPONENT_NAME=		camlp4
COMPONENT_VERSION=	4.02
IPS_COMPONENT_VERSION=	4.0.2
COMPONENT_PROJECT_URL=	https://opam.ocaml.org
COMPONENT_FMRI=		library/ocaml/camlp4
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_VERSION).zip
COMPONENT_ARCHIVE_HASH=	\
	sha256:8dbf6bcf11883517a937bae4842467f23634b48115f01ab12dd887dafed5c662
COMPONENT_ARCHIVE_URL=	https://github.com/ocaml/camlp4/archive/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	LGPLv2
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=	Camlp4 tool
COMPONENT_CLASSIFICATION=Development/Other Languages

CONFIGURE_DEFAULT_DIRS=no

include ../../../make-rules/prep.mk
include ../../../make-rules/configure.mk
include ../../../make-rules/ips.mk

CONFIGURE_OPTIONS  = --bindir=$(CONFIGURE_PREFIX)/bin
CONFIGURE_OPTIONS += --libdir=$(CONFIGURE_PREFIX)/lib/ocaml
CONFIGURE_OPTIONS += --pkgdir=$(CONFIGURE_PREFIX)/lib

COMPONENT_PRE_CONFIGURE_ACTION=$(CLONEY) $(SOURCE_DIR) $(@D)

COMPONENT_BUILD_TARGETS=byte

build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(TEST_32)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS) ocaml

include ../../../make-rules/depend.mk
