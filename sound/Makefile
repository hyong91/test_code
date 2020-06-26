SRC_C=$(wildcard *.c)

INC +=  $(addprefix -I, $(shell find ./include -type d))
CC = /home/linux/samba/test/rk3308/buildroot/output/tuya_rk3308_smartspeaker_avs_release/host/bin/aarch64-rockchip-linux-gnu-gcc
AR = /home/linux/samba/test/rk3308/buildroot/output/tuya_rk3308_smartspeaker_avs_release/host/bin/aarch64-rockchip-linux-gnu-ar
TOPDIR = /home/linux/samba/test/rk3308/buildroot
INC += -I $(TOPDIR)/output/tuya_rk3308_smartspeaker_avs_release/host/aarch64-rockchip-linux-gnu/sysroot/usr/include

LIBS_CC = -lm -lpthread -lasound -ldl

HAL_LIB_DIR = -L$(TOPDIR)/output/tuya_rk3308_smartspeaker_avs_release/target/usr/lib
HAL_LIB_DIR += -L$(TOPDIR)/output/tuya_rk3308_smartspeaker_avs_release/target/lib

TARGET=lplay lrecord

all: $(TARGET)
	
lrecord : lrecord.c wav_parser.c sndwav_common.c
	$(CC) $(CFLAGS) -o $@ $^ $(INC) $(HAL_LIB_DIR) $(LIBS_CC)

lplay : lplay.c wav_parser.c sndwav_common.c
	$(CC) $(CFLAGS) -o $@ $^ $(INC) $(HAL_LIB_DIR) $(LIBS_CC)

clean:
	rm -rf *.o $(TARGET)

