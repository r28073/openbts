#
# Copyright 2008, 2009 Free Software Foundation, Inc.
# Copyright 2011, 2012 Range Networks, Inc.
#
# This software is distributed under the terms of the GNU Public License.
# See the COPYING file in the main directory for details.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.
#

include $(top_srcdir)/Makefile.common

AM_CPPFLAGS = $(STD_DEFINES_AND_INCLUDES)
AM_CXXFLAGS = -Wall -O3 -g -ldl -lpthread

noinst_LTLIBRARIES = libGSMShare.la

libGSMShare_la_SOURCES = \
	AmrCoder.cpp \
	GSM503Tables.cpp \
	ViterbiR204.cpp \
	A51.cpp

noinst_PROGRAMS = \
	ViterbiTest \
	AMRTest \
	A51Test

#	ReportingTest 

noinst_HEADERS = \
	Viterbi.h \
	ViterbiR204.h \
	AmrCoder.h \
	ViterbiR204.h \
	GSM503Tables.h \
	A51.h

# (pat 8-2013) I dont know how to properly include the CommonLibs directory using autofoo.  You are welcome to correct this reference.
ViterbiTest_SOURCES = AMRTest.cpp
ViterbiTest_LDADD = $(noinst_LTLIBRARIES) ../CommonLibs/libcommon.la

AMRTest_SOURCES = AMRTest.cpp
AMRTest_LDADD = $(noinst_LTLIBRARIES) ../CommonLibs/libcommon.la

A51Test_SOURCES = A51Test.cpp
A51Test_LDADD = $(noinst_LTLIBRARIES) ../CommonLibs/libcommon.la

