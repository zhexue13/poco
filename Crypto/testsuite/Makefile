#
# Makefile
#
# Makefile for Poco Crypto testsuite
#

include $(POCO_BASE)/build/rules/global

include $(POCO_BASE)/build/script/openssl_ver

# Note: linking order is important, do not change it.
ifeq ($(POCO_CONFIG),FreeBSD)
SYSLIBS += -lssl -lcrypto -lz
else
SYSLIBS += -lssl -lcrypto -lz -ldl
endif

objects = CryptoTestSuite Driver \
	CryptoTest DigestEngineTest ECTest \
	EVPTest RSATest PKCS12ContainerTest

target         = testrunner
target_version = 1
target_libs    = PocoCrypto PocoFoundation PocoCppUnit

include $(POCO_BASE)/build/rules/exec
