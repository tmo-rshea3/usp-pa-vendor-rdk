AM_CPPFLAGS = -I$(SYSROOT)$(includedir)/obuspa \
              -I$(SYSROOT)$(includedir)/obuspa/internal \
              -I$(SYSROOT)$(includedir)/rbus

AM_CFLAGS = -Wall -Wfatal-errors
AM_LDFLAGS =

# Hardening
AM_CFLAGS += $(CFLAGS_HARDENING)
AM_LDFLAGS += $(LDFLAGS_HARDENING)

pkglib_LTLIBRARIES = usp-pa-vendor-rdk.la

usp_pa_vendor_rdk_la_SOURCES = vendor.c
usp_pa_vendor_rdk_la_CPPFLAGS = $(AM_CPPFLAGS) \
                                -Werror \
                                -Werror=unused-value \
                                -Werror=format \
                                -Winit-self \
                                -Wparentheses -Werror=parentheses \
                                -Wuninitialized -Werror=uninitialized -Werror=maybe-uninitialized -Wpointer-arith

usp_pa_vendor_rdk_la_LDFLAGS = $(AM_LDFLAGS) -avoid-version -module -shared -export-dynamic
usp_pa_vendor_rdk_la_LDFLAGS += -lrbus
