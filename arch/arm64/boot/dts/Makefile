ifneq ($(filter MSM_17011 MSM_17015 MSM_17081 MSM_17085, $(OPPO_TARGET_DEVICE)),)
	dts-dirs += 17011
	dts-dirs += 17021
else
	dts-dirs += 16051
	dts-dirs += 16103
	dts-dirs += 16118
endif

subdir-y	:= $(dts-dirs)

dtstree		:= $(srctree)/$(src)

dtb-$(CONFIG_OF_ALL_DTBS) := $(patsubst $(dtstree)/%.dts,%.dtb, $(foreach d,$(dts-dirs), $(wildcard $(dtstree)/$(d)/*.dts)))

always		:= $(dtb-y)
targets += dtbs