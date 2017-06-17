NAME = terraform
VERSION = 0.9.8
FPM_SOURCE = dir
SOURCE_URL = https://releases.hashicorp.com/$(NAME)/$(VERSION)/$(NAME)_$(VERSION)_linux_amd64.zip
SRC_ZIP = $(notdir $(SOURCE_URL))
PACKAGE_URL = https://www.terraform.io/
PACKAGE_DESCRIPTION = Open source tool that codifies APIs into declarative configuration files that can be shared amongst team members, treated as code, edited, reviewed, and versioned

include ../include/base.mk

extract: fetch default_build
	cd $(BUILDDIR); unzip $(CACHEDIR)/$(SRC_ZIP)

build: extract
	mkdir -p $(DESTDIR)/usr/local \
	  && cp -pR $(BUILDDIR)/terraform $(DESTDIR)/usr/local/$(NAME)
