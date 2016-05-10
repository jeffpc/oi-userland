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

COMPONENT_NAME=		ocaml
COMPONENT_VERSION=	4.02.1
IPS_COMPONENT_VERSION=	4.0.2.1
COMPONENT_PROJECT_URL=	https://ocaml.org/
COMPONENT_FMRI=		runtime/ocaml
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.xz
COMPONENT_ARCHIVE_HASH=	\
	sha256:68c4b01be54c23bc20fc0a8beaa5c7433b8483f8950490129cfe7662e0c6f4dc
COMPONENT_ARCHIVE_URL=	http://caml.inria.fr/pub/distrib/ocaml-4.02/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	Q+GPLv2
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=	OCaml is a programming language supporting functional, imperative and object-oriented styles
COMPONENT_CLASSIFICATION=Development/Other Languages

CONFIGURE_DEFAULT_DIRS=no

include ../../../make-rules/prep.mk
include ../../../make-rules/configure.mk
include ../../../make-rules/ips.mk

CONFIGURE_OPTIONS  = -prefix $(CONFIGURE_PREFIX)
CONFIGURE_OPTIONS += -mandir $(CONFIGURE_PREFIX)/share/man/man1
#CONFIGURE_OPTIONS += -with-frame-pointers

COMPONENT_PRE_CONFIGURE_ACTION=$(CLONEY) $(SOURCE_DIR) $(@D)

COMPONENT_BUILD_TARGETS=world opt opt.opt

build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(TEST_32)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS)

include ../../../make-rules/depend.mk
