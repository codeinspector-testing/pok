export POK_PATH=$(CURDIR)/../../../../
export ARCH=x86
export BSP=x86-qemu
export DEPLOYMENT_HEADER=$(shell pwd)/deployment.h

include $(POK_PATH)/misc/mk/config.mk

TARGET	=  pr2.elf
OBJS		=	main.o subprograms.o activity.o ../../receive.o

all: libpok $(TARGET)

.PHONY: clean distclean install all

clean: common-clean

distclean: clean
	$(RM) .depend.mk

include $(POK_PATH)/misc/mk/common-$(ARCH).mk
include $(POK_PATH)/misc/mk/rules-common.mk
include $(POK_PATH)/misc/mk/rules-partition.mk
