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

include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		file
COMPONENT_VERSION=	5.23
COMPONENT_PROJECT_URL=	http://darwinsys.com/file/
COMPONENT_FMRI=		file/file
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	\
	sha256:2c8ab3ff143e2cdfb5ecee381752f80a79e0b4cfe9ca4cc6e1c3e5ec15e6157c
COMPONENT_ARCHIVE_URL=	ftp://ftp.astron.com/pub/file/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	BSD
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=	a file type guesser
COMPONENT_CLASSIFICATION=Applications/System Utilities

include ../../make-rules/prep.mk
include ../../make-rules/configure.mk
include ../../make-rules/ips.mk

build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(TEST_32)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS)

include ../../make-rules/depend.mk
