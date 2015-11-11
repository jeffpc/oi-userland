#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2015 Josef 'Jeff' Sipek <jeffpc@josefsipek.net>
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		gcc-links
COMPONENT_VERSION=	0.1
COMPONENT_PROJECT_URL=		
COMPONENT_FMRI=		developer/gcc-links
COMPONENT_CLASSIFICATION="Development/C"

include ../../make-rules/prep.mk
include ../../make-rules/ips.mk

$(BUILD_DIR)/%/.built:
	$(MKDIR) $(@D)
	$(TOUCH) $@

$(BUILD_DIR)/%/.installed:	$(BUILD_DIR)/%/.built
	$(TOUCH) $@

build: $(BUILD_32)

install: $(INSTALL_32)
