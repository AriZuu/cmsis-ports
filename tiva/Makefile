#
# Copyright (c) 2012-2014, Ari Suutari <ari@stonepile.fi>.
# All rights reserved. 
# 
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
# 
#  1. Redistributions of source code must retain the above copyright
#     notice, this list of conditions and the following disclaimer.
#  2. Redistributions in binary form must reproduce the above copyright
#     notice, this list of conditions and the following disclaimer in the
#     documentation and/or other materials provided with the distribution.
#  3. The name of the author may not be used to endorse or promote
#     products derived from this software without specific prior written
#     permission. 
# 
# THIS SOFTWARE IS PROVIDED BY THE AUTHOR ``AS IS'' AND ANY EXPRESS
# OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
# WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
# ARE DISCLAIMED. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT,
# INDIRECT,  INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
# (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
# SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
# HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT,
# STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
# ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED
# OF THE POSSIBILITY OF SUCH DAMAGE.

DIST = tmp

DISTCLEAN_EXTRA += tivaware
include ../Makefile.inc1

extract: inc/system_TM4C129.h

inc/system_TM4C129.h:
	mkdir -p inc
	mkdir -p src
	mkdir -p tivaware/inc
	mkdir -p tivaware/driverlib
	mkdir -p tmp
	(cd tmp; unzip -q -aa ../../$(DISTFILES)/speters-cmsis.zip)
	(cd tmp; unzip -q -aa ../../$(DISTFILES)/antoinealb-tivaware.zip)
	cp $(DIST)/CMSIS-master/Device/TI/TM4C/Include/*.h inc/
	cp $(DIST)/CMSIS-master/Device/TI/TM4C/Source/*.c src/
	cp $(DIST)/Tivaware-master/inc/*.h tivaware/inc/
	cp $(DIST)/Tivaware-master/driverlib/*.* tivaware/driverlib/
	rm -f tivaware/driverlib/onewire.c
	rm -rf tmp

