/*---------------------------- 2019/7/19-----------------------------------------------------/
1，添加支持smdk2440
	一，修改boards.cfg
		make smdk2440_deconfig
			uboot2012.04.01$ cat include/config.h
			/* Automatically generated - do not edit */
			#define CONFIG_BOARDDIR board/samsung/smdk2440
			#include <config_cmd_defaults.h>
			#include <config_defaults.h>
			#include <configs/smdk2440.h>
			#include <asm/config.h>
		发现需要创建 board/samsung/smdk2440, configs/smdk2440.h 文件 
	二，复制 board/samsung/smdk2410  board/samsung/smdk2440
	三，修改 board/samsung/smdk2440 
		smdk2440.c Makefile
	四，复制 include/configs/smdk2410.h include/configs/smdk2440.h
/*-------------------------------------------------------------------------------------------/