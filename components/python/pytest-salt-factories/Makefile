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
# This file was automatically generated using the following command:
#   $WS_TOOLS/python-integrate-project -d python/pytest-salt-factories pytest_salt_factories
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		pytest_salt_factories
HUMAN_VERSION =			1.0.4
COMPONENT_SUMMARY =		Pytest Salt Plugin
COMPONENT_PROJECT_URL =		https://github.com/saltstack/pytest-salt-factories
COMPONENT_ARCHIVE_HASH =	\
	sha256:4532a74a8195353dc094fa620870dff76d1c4fc9ce38c4a4c6470297849dc178
COMPONENT_LICENSE =		Apache-2.0
COMPONENT_LICENSE_FILE =	LICENSE

TEST_STYLE = pytest

include $(WS_MAKE_RULES)/common.mk

# This project does not support tox so we need to provide test requirements
# manually.
TEST_REQUIREMENTS += requirements/tests.txt

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/attrs
PYTHON_REQUIRED_PACKAGES += library/python/msgpack
PYTHON_REQUIRED_PACKAGES += library/python/psutil
PYTHON_REQUIRED_PACKAGES += library/python/pytest
PYTHON_REQUIRED_PACKAGES += library/python/pytest-helpers-namespace
PYTHON_REQUIRED_PACKAGES += library/python/pytest-shell-utilities
PYTHON_REQUIRED_PACKAGES += library/python/pytest-skip-markers
PYTHON_REQUIRED_PACKAGES += library/python/pytest-system-statistics
PYTHON_REQUIRED_PACKAGES += library/python/pyyaml
PYTHON_REQUIRED_PACKAGES += library/python/pyzmq
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += library/python/setuptools-declarative-requirements
PYTHON_REQUIRED_PACKAGES += library/python/setuptools-scm
PYTHON_REQUIRED_PACKAGES += library/python/virtualenv
PYTHON_REQUIRED_PACKAGES += library/python/wheel
PYTHON_REQUIRED_PACKAGES += runtime/python
TEST_REQUIRED_PACKAGES.python += library/python/attrs
TEST_REQUIRED_PACKAGES.python += library/python/importlib-metadata
TEST_REQUIRED_PACKAGES.python += library/python/msgpack
TEST_REQUIRED_PACKAGES.python += library/python/psutil
TEST_REQUIRED_PACKAGES.python += library/python/pyfakefs
TEST_REQUIRED_PACKAGES.python += library/python/pytest
TEST_REQUIRED_PACKAGES.python += library/python/pytest-helpers-namespace
TEST_REQUIRED_PACKAGES.python += library/python/pytest-shell-utilities
TEST_REQUIRED_PACKAGES.python += library/python/pytest-skip-markers
TEST_REQUIRED_PACKAGES.python += library/python/pytest-subtests
TEST_REQUIRED_PACKAGES.python += library/python/pytest-system-statistics
TEST_REQUIRED_PACKAGES.python += library/python/pyyaml
TEST_REQUIRED_PACKAGES.python += library/python/pyzmq
TEST_REQUIRED_PACKAGES.python += library/python/virtualenv
