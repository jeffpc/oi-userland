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
# Copyright 2014 Alexander Pyhalov.  All rights reserved.
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME= 	maven
COMPONENT_VERSION= 3.2.3
COMPONENT_FMRI= developer/build/maven
COMPONENT_CLASSIFICATION = Development/Java
COMPONENT_PROJECT_URL = http://maven.apache.org
COMPONENT_SRC= apache-maven-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_SRC)-bin.tar.gz
COMPONENT_ARCHIVE_HASH= \
  sha256:bf3f04aadee3a67158aebdfb0b4cb022063329d459d10fd6b4b02223e10aa8ed
COMPONENT_ARCHIVE_URL= \
  http://apache-mirror.rbc.ru/pub/apache/maven/maven-3/$(COMPONENT_VERSION)/binaries/$(COMPONENT_ARCHIVE)
COMPONENT_SUMMARY= Apache Maven is a software project management and comprehension tool

include ../../make-rules/prep.mk
include ../../make-rules/ips.mk

build:

install: prep
	[ -d $(PROTO_DIR)/usr/share/maven ] || mkdir -p $(PROTO_DIR)/usr/share/maven
	cp -r $(SOURCE_DIR)/* $(PROTO_DIR)/usr/share/maven/

clean::
	rm -rf $(BUILD_DIR)
