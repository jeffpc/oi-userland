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
# Copyright (c) 2015 Alexander Pyhalov
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME=           dcraw
COMPONENT_VERSION=        8.99
COMPONENT_PROJECT_URL=    https://www.cybercom.net/~dcoffin/dcraw/
COMPONENT_SUMMARY=        dcraw - Decoding RAW digital photos
COMPONENT_SRC=            $(COMPONENT_NAME)
COMPONENT_ARCHIVE=        $(COMPONENT_NAME)-$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH=        \
    sha256:f8c64153998c375390cd24d9695701c7d71773d810fece8c31da2199353da570
#COMPONENT_ARCHIVE_URL=        http://cybercom.net/~dcoffin/dcraw/archive/$(COMPONENT_ARCHIVE)
COMPONENT_ARCHIVE_URL=        http://dlc.openindiana.org/oi/jds/downloads/sources/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	GPLv2
COMPONENT_LICENSE_FILE=	dcraw.license
COMPONENT_FMRI=		image/dcraw
COMPONENT_CLASSIFICATION=	System/Media

include $(WS_TOP)/make-rules/prep.mk
include $(WS_TOP)/make-rules/justmake.mk
include $(WS_TOP)/make-rules/ips.mk

COMPONENT_BUILD_ARGS += CC=$(CC)
COMPONENT_BUILD_ARGS += CXX=$(CXX)
COMPONENT_BUILD_ARGS += CFLAGS="$(CFLAGS)"
                                        
# common targets
build:                $(BUILD_32)

install:        $(INSTALL_32)

test:                $(NO_TESTS)

BUILD_PKG_DEPENDENCIES = $(BUILD_TOOLS)

include $(WS_TOP)/make-rules/depend.mk
