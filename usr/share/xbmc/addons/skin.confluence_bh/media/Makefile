TARGET=Textures.xbt
XBMCTEX=/Abuild2/Elmo/setup-script/build/tmp-angstrom_v2012_12-eglibc/work/elmo-angstrom-linux-gnueabi/xbmc-12.0-r0+gitr1+51d02c2556214761d001ff2faee0f411d5c88efb/git/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
ifeq (,1)
	$(XBMCTEX) -use_none -input . -output $(TARGET)
else
	$(XBMCTEX) -input . -output $(TARGET)

endif
$(XBMCTEX): force
	$(MAKE) -C /Abuild2/Elmo/setup-script/build/tmp-angstrom_v2012_12-eglibc/work/elmo-angstrom-linux-gnueabi/xbmc-12.0-r0+gitr1+51d02c2556214761d001ff2faee0f411d5c88efb/git/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

