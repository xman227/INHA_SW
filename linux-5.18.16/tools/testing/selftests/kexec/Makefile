# SPDX-License-Identifier: GPL-2.0-only
# Makefile for kexec tests

uname_M := $(shell uname -m 2>/dev/null || echo not)
ARCH ?= $(shell echo $(uname_M) | sed -e s/i.86/x86/ -e s/x86_64/x86/)

ifeq ($(ARCH),$(filter $(ARCH),x86 ppc64le))
TEST_PROGS := test_kexec_load.sh test_kexec_file_load.sh
TEST_FILES := kexec_common_lib.sh

include ../lib.mk

endif
