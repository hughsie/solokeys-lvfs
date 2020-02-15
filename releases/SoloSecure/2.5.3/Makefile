# Copyright (C) 2016 Richard Hughes <richard@hughsie.com>

VENDOR=SoloKeys
PROJECT_NAME=Secure
VERSION=2.5.3
FIRMWARE_FILES=				\
	firmware-secure-2.5.3.json
METAINFO_FILES=				\
	com.solokeys.secure.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
