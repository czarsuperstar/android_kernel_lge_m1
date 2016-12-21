Kernel Build  
  - Uncompress using following command at the android directory
        tar xvzf LGMS330_L_Kernel.tar.gz
  - When you compile the kernel source code, you have to add google original prebuilt source(toolchain) into the android directory.
  - Run following scripts to build kernel
  
  - cd kernel
  - export ARCH=arm
  - export TARGET_PRODUCT=m1_mpcs_us
  - export CROSS_COMPILE=../prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/bin/arm-eabi-  
  - make m1_mpcs_us_defconfig
  - make zImage
    
    * "-j4" : The number, 4, is the number of multiple jobs to be invoked simultaneously. 
	* lz4demo : More information can be found at "https://code.google.com/p/lz4/"		 
  - After build, you can find the build image(zImage) at arch/arm/boot


