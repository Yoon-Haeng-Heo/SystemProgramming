KERNEL_DIR = /lib/modules/4.19.97-v7+/build

obj-m := light_dev.o sound_dev.o gas_dev.o temp_dev.o

PWD := $(shell pwd)

all:
	make -C $(KERNEL_DIR) M=$(PWD) modules

clean:
	make -C $(KERNEL_DIR) M=$(PWD) clean

app:
	gcc -o app app.c -L../libs -lmynet -W -Wall -pthread -lm