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

USE_DEFAULT_TEST_TRANSFORMS= yes
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		cracklib
COMPONENT_VERSION=	2.10.3
COMPONENT_SUMMARY=	CrackLib Library and Dictionaries
COMPONENT_PROJECT_URL=	https://github.com/cracklib/cracklib
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.bz2
COMPONENT_ARCHIVE_HASH= sha256:f3dcb54725d5604523f54a137b378c0427c1a0be3e91cfb8650281a485d10dae
COMPONENT_ARCHIVE_URL=	https://github.com/cracklib/cracklib/releases/download/v$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_FMRI=		library/security/cracklib
COMPONENT_CLASSIFICATION=	System/Libraries
COMPONENT_LICENSE=	LGPLv2.1
COMPONENT_LICENSE_FILE=	COPYING.LIB

include $(WS_MAKE_RULES)/common.mk

CFLAGS += $(XPG6MODE)
CFLAGS += -D_POSIX_PTHREAD_SEMANTICS

CONFIGURE_OPTIONS += --disable-static
CONFIGURE_OPTIONS += --without-python

# Auto-generated dependencies
REQUIRED_PACKAGES += library/zlib
REQUIRED_PACKAGES += shell/ksh93
REQUIRED_PACKAGES += system/library
