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

COMPONENT_NAME=		opam
COMPONENT_VERSION=	1.2.2
COMPONENT_PROJECT_URL=	https://opam.ocaml.org
COMPONENT_FMRI=		library/ocaml/opam
COMPONENT_SRC=		$(COMPONENT_NAME)-full-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	\
	sha256:15e617179251041f4bf3910257bbb8398db987d863dd3cfc288bdd958de58f00
COMPONENT_ARCHIVE_URL=	https://github.com/ocaml/opam/releases/download/$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	GPLv3+LGPLv3
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=	OCaml Package Manager 
COMPONENT_CLASSIFICATION=Development/Other Languages

CONFIGURE_DEFAULT_DIRS=no

include ../../../make-rules/prep.mk
include ../../../make-rules/configure.mk
include ../../../make-rules/ips.mk

COMPONENT_PRE_CONFIGURE_ACTION=$(CLONEY) $(SOURCE_DIR) $(@D)

COMPONENT_BUILD_TARGETS=lib-ext all

build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(TEST_32)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS) ocaml

include ../../../make-rules/depend.mk
