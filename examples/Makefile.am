# ngtcp2

# Copyright (c) 2017 ngtcp2 contributors

# Permission is hereby granted, free of charge, to any person obtaining
# a copy of this software and associated documentation files (the
# "Software"), to deal in the Software without restriction, including
# without limitation the rights to use, copy, modify, merge, publish,
# distribute, sublicense, and/or sell copies of the Software, and to
# permit persons to whom the Software is furnished to do so, subject to
# the following conditions:

# The above copyright notice and this permission notice shall be
# included in all copies or substantial portions of the Software.

# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
# EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
# MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
# NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
# LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
# OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
# WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

AM_CFLAGS = $(WARNCFLAGS) $(DEBUGCFLAGS)
AM_CXXFLAGS = $(WARNCXXFLAGS) $(DEBUGCFLAGS)
AM_CPPFLAGS = \
	-I$(top_srcdir)/lib/includes \
	-I$(top_builddir)/lib/includes \
	-I$(top_srcdir)/third-party \
	@OPENSSL_CFLAGS@ \
	@LIBEV_CFLAGS@ \
	@LIBMYSQLCLIENT_CFLAGS@ \
	@DEFS@
AM_LDFLAGS = -no-install
LDADD = $(top_builddir)/lib/libngtcp2.la \
	$(top_builddir)/third-party/libhttp-parser.la \
	@OPENSSL_LIBS@ \
	@LIBEV_LIBS@ \
	@LIBMYSQLCLIENT_LIBS@

noinst_PROGRAMS = client server balancer balancer2

client_SOURCES = client.cc client.h \
	template.h \
	debug.cc debug.h \
	util.cc util.h \
	shared.h \
	crypto_openssl.cc \
	crypto.cc

server_SOURCES = server.cc server.h \
	template.h \
	debug.cc debug.h \
	util.cc util.h \
	shared.h \
	crypto_openssl.cc \
	crypto.cc \
	http.cc http.h

balancer_SOURCES = balancer.cc balancer.h \
	template.h \
	debug.cc debug.h \
	util.cc util.h \
	shared.h \
	crypto_openssl.cc \
	crypto.cc \
	http.cc http.h

balancer2_SOURCES = balancer2.cc balancer.h \
	template.h \
	debug.cc debug.h \
	util.cc util.h \
	shared.h \
	crypto_openssl.cc \
	crypto.cc \
	http.cc http.h
