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
#   $WS_TOOLS/python-integrate-project aiohttp
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		aiohttp
HUMAN_VERSION =			3.11.9
COMPONENT_SUMMARY =		Async http client/server framework (asyncio)
COMPONENT_PROJECT_URL =		https://github.com/aio-libs/aiohttp
COMPONENT_ARCHIVE_HASH =	\
	sha256:a9266644064779840feec0e34f10a89b3ff1d2d6b751fe90017abcad1864fa7c
COMPONENT_LICENSE =		Apache-2.0
COMPONENT_LICENSE_FILE =	LICENSE.txt

TEST_STYLE = pytest

include $(WS_MAKE_RULES)/common.mk

# This project does not support tox so we need to provide test requirements
# manually.
TEST_REQUIREMENTS += requirements/test.in

#
# Tests are run from build directory that contains cloned copy of sdist.  We
# try to ask Python to find tested modules in the proto area (the PYTHONPATH is
# set accordingly), but Python (< 3.11) always adds the current directory to
# sys.path and there is no known (simple) way how to avoid that.  Except -I,
# but that would cause Python to ignore PYTHONPATH too so we would not have
# access to the proto area either.  The -P option together with PYTHONSAFEPATH
# environment variable were added to Python 3.11 only so we cannot use them yet
# for all Python versions we support.
#
# Since sdist for this project contains the main module in the top-level
# directory we cannot force Python to skip it.  But, unfortunately, this module
# does not contain built dynamic libraries, so Python cannot find them while
# testing.
#
# To workaround this we rename the main module in the build directory during
# testing so Python will need to defer to PYTHONPATH.
#
COMPONENT_PRE_TEST_ACTION +=	$(MV) $(@D)/aiohttp $(@D)/aiohttp-RENAMED ;
COMPONENT_POST_TEST_ACTION +=	$(MV) $(@D)/aiohttp-RENAMED $(@D)/aiohttp ;

# We need to ignore tests in test_proxy_functional.py because we do not have
# the proxy.py Python project packaged yet.
PYTEST_ADDOPTS += --ignore tests/test_proxy_functional.py
# We have no python-on-whales packaged yet.
PYTEST_ADDOPTS += --ignore tests/autobahn/test_autobahn.py
# We have no pytest_codspeed packaged yet so we cannot run benchmark tests.
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_cookiejar.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_client_request.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_http_writer.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_http_websocket.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_client.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_client_ws.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_web_middleware.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_web_response.py
PYTEST_ADDOPTS += --ignore tests/test_benchmarks_web_urldispatcher.py

# Random directory name
COMPONENT_TEST_TRANSFORMS += "-e 's|/tmp/.*/garbage[^/]*|\$$(TMPDIR)|'"

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/aiohappyeyeballs
PYTHON_REQUIRED_PACKAGES += library/python/aiosignal
PYTHON_REQUIRED_PACKAGES += library/python/async-timeout
PYTHON_REQUIRED_PACKAGES += library/python/attrs
PYTHON_REQUIRED_PACKAGES += library/python/frozenlist
PYTHON_REQUIRED_PACKAGES += library/python/multidict
PYTHON_REQUIRED_PACKAGES += library/python/propcache
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += library/python/yarl
PYTHON_REQUIRED_PACKAGES += runtime/python
REQUIRED_PACKAGES += system/library
TEST_REQUIRED_PACKAGES.python += library/python/aiohappyeyeballs
TEST_REQUIRED_PACKAGES.python += library/python/aiosignal
TEST_REQUIRED_PACKAGES.python += library/python/async-timeout
TEST_REQUIRED_PACKAGES.python += library/python/attrs
TEST_REQUIRED_PACKAGES.python += library/python/brotli
TEST_REQUIRED_PACKAGES.python += library/python/coverage
TEST_REQUIRED_PACKAGES.python += library/python/freezegun
TEST_REQUIRED_PACKAGES.python += library/python/frozenlist
TEST_REQUIRED_PACKAGES.python += library/python/gunicorn
TEST_REQUIRED_PACKAGES.python += library/python/multidict
TEST_REQUIRED_PACKAGES.python += library/python/mypy
TEST_REQUIRED_PACKAGES.python += library/python/propcache
TEST_REQUIRED_PACKAGES.python += library/python/pytest
TEST_REQUIRED_PACKAGES.python += library/python/pytest-cov
TEST_REQUIRED_PACKAGES.python += library/python/pytest-mock
TEST_REQUIRED_PACKAGES.python += library/python/pytest-xdist
TEST_REQUIRED_PACKAGES.python += library/python/re-assert
TEST_REQUIRED_PACKAGES.python += library/python/trustme
TEST_REQUIRED_PACKAGES.python += library/python/yarl
