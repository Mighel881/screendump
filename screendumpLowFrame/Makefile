TARGET = iphone:11.2:10.0

include $(THEOS)/makefiles/common.mk


TOOL_NAME = screendumpd
$(TOOL_NAME)_FILES = /mnt/d/codes/screendumpLowFrame/main.mm
$(TOOL_NAME)_FRAMEWORKS := IOSurface IOKit
$(TOOL_NAME)_PRIVATE_FRAMEWORKS := IOMobileFramebuffer IOSurface
$(TOOL_NAME)_OBJCFLAGS += -I/mnt/d/codes/screendumpLowFrame/vncbuild/include -Iinclude
$(TOOL_NAME)_LDFLAGS += -Wl,-segalign,4000 -L/mnt/d/codes/screendumpLowFrame/vncbuild/lib  -lvncserver -lpng -llzo2 -ljpeg -lssl -lcrypto -lz
$(TOOL_NAME)_CFLAGS = -w
export ARCHS = arm64
$(TOOL_NAME)_ARCHS = arm64
$(TOOL_NAME)_CODESIGN_FLAGS = "-Sen.plist"
$(TOOL_NAME)_INSTALL_PATH = /usr/libexec

include $(THEOS_MAKE_PATH)/tool.mk


SUBPROJECTS += hooks

include $(THEOS_MAKE_PATH)/aggregate.mk
