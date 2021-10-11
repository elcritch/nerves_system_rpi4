#
# Zhangqun Ming <north_sea@qq.com>
# Copyright (c) 2021 Seeed Studio
#
# MIT License
#
# KVERSION ?= $(shell uname -r)

obj-m := mipi_dsi_ili9881d.o
mipi_dsi_ili9881d-objs := mipi_dsi_drv.o		\
				 touch_panel.o		\
				 panel-ili9881d.o

ccflags-y := -DDEBUG -g -std=gnu99 -Werror -Wno-declaration-after-statement -Wframe-larger-than=1000000000

.PHONY: all clean

modules:
	$(MAKE) -C ‘$(LINUX_DIR)’ M=’$(PWD)’ modules

all:
	$(MAKE) -C '$(LINUX_DIR)' M='$(PWD)' modules

clean:
	$(MAKE) -C '$(LINUX_DIR)' M='$(PWD)' clean