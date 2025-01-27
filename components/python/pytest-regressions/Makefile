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
#   $WS_TOOLS/python-integrate-project -d python/pytest-regressions pytest_regressions
#

BUILD_STYLE = setup.py

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		pytest_regressions
HUMAN_VERSION =			2.7.0
COMPONENT_SUMMARY =		Easy to use fixtures to write regression tests.
COMPONENT_PROJECT_URL =		https://github.com/ESSS/pytest-regressions
COMPONENT_ARCHIVE_HASH =	\
	sha256:4c30064e0923929012c94f5d6f35205be06fd8709c7f0dba0228e05c460af05e
COMPONENT_LICENSE =		MIT
COMPONENT_LICENSE_FILE =	LICENSE

include $(WS_MAKE_RULES)/common.mk

# We have no pandas packaged yet
PYTEST_ADDOPTS += --ignore tests/test_dataframe_regression.py
PYTEST_ADDOPTS += --ignore tests/test_filenames.py
PYTEST_ADDOPTS += --ignore tests/test_num_regression.py

# We have no matplotlib packaged yet
PYTEST_ADDOPTS += --deselect tests/test_image_regression.py::test_image_regression

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/pytest
PYTHON_REQUIRED_PACKAGES += library/python/pytest-datadir
PYTHON_REQUIRED_PACKAGES += library/python/pyyaml
PYTHON_REQUIRED_PACKAGES += runtime/python
TEST_REQUIRED_PACKAGES.python += library/python/mypy
TEST_REQUIRED_PACKAGES.python += library/python/numpy
TEST_REQUIRED_PACKAGES.python += library/python/pillow
