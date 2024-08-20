# GBDK2020 COMPILE FLAGS - GAME BOY

<br><br>



## LCC FLAGS



---
**-Wm-y**
- set rom headers 

```makefile
-Wm-yn"$(NAME)"                         # set rom header name ????

-Wm-yc                                  # normal speed for GBC, allows use of cpu_fast()
-Wm-yC                                  # double speed, for GBC only
```



---
**-Wl-y**
- set MBC type
- check GBDK2020 docs `6.2.4 MBC Type Chart` for more options and configurations

```makefile
-Wl-yt0x12                              # MBC3
-Wl-yt0x19                              # MBC5

-Wl-yo8                                 # 256KB ROM (8 banks)
-Wl-yo16                                # 512KB ROM (16 banks)
-Wl-yo64                                # 1MB ROM (64 banks)
-Wl-yo128                               # 2MB ROM (128 banks)

-Wl-ya2                                 # 8KB SRAM (2 banks)
-Wl-ya4                                 # 16KB SRAM (4 banks)
-Wl-ya8                                 # 32KB SRAM (8 banks)
-Wl-ya16                                # 64KB SRAM (16 banks)
```



---
**-debug**
- builds files needed for degugging

```makefile
-debug                                  # equivalent to -Wl-j, -Wa-l, -Wm-yS ????
```



---
**-Wf-I**
- tell linker to check directory for include files

```makefile
-Wf-Iinclude                            # check ./include for .h files
-Wf-Iinclude/assets                     # check ./include/assets for .h files
-Wf-Isrc                                # check ./src for .h files
```



---
**-Wl-l**
- tell linker to link things ????

```makefile
-Wl-lhuge/hUGEDriver.lib                # link ./huge/huge-driver.lib during compiling
```



## TODO

- -autobank
- -Wf-MMD
- -Wl-j 
- -Wb-ext=.rel
- -Wb-v
- ... others

