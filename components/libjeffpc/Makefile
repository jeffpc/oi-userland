#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL)". You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright (c) 2016 Josef 'Jeff' Sipek <jeffpc@josefsipek.net>
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		libjeffpc
COMPONENT_FMRI=		library/jeffpc
COMPONENT_VERSION=	0.10
COMPONENT_PROJECT_URL=	https://github.com/jeffpc/libjeffpc
COMPONENT_SUMMARY=	jeffpc helper library
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	v$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH=	\
    sha256:99e59848bf7c749aaec02d9c12c0fe07b354e542425d2f2f8a162a2b367a5a33
COMPONENT_ARCHIVE_URL=	https://github.com/jeffpc/libjeffpc/archive/$(COMPONENT_ARCHIVE)
COMPONENT_CLASSIFICATION=System/Libraries
COMPONENT_LICENSE=MIT
COMPONENT_LICENSE_FILE=$(COMPONENT_NAME).license

include ../../make-rules/prep.mk
include ../../make-rules/cmake.mk
include ../../make-rules/ips.mk

build:		$(BUILD_32_and_64)

install:	$(INSTALL_32_and_64)

test:		$(TEST_32_and_64)

BUILD_PKG_DEPENDENCIES =	$(BUILD_TOOLS)

include ../../make-rules/depend.mk
