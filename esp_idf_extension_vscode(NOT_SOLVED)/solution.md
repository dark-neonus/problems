Trying to use `ESP IDF` extension for VS code to build and flash code to my `esp32 WROOM`.

Right now I tried to install `ESP IDF` using menu inside VS code to install `ESP IDF`.
After that I opend `blink` example and tried to build. I encounter error:

```log
 *  Executing task: ninja  

[0/1] Re-running CMake...
-- git rev-parse returned 'fatal: not a git repository (or any parent up to mount point /mnt)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).'
-- Could not use 'git describe' to determine PROJECT_VER.
-- Building ESP-IDF components for target esp32
NOTICE: Processing 2 dependencies:
NOTICE: [1/2] espressif/led_strip (2.5.5)
NOTICE: [2/2] idf (5.4.1)
-- Project sdkconfig file /mnt/D/code/hardware/blink/sdkconfig
Loading defaults file /mnt/D/code/hardware/blink/sdkconfig.defaults...
Loading defaults file /mnt/D/code/hardware/blink/sdkconfig.defaults.esp32...
-- Compiler supported targets: xtensa-esp-elf
-- App "blink" version: 1
-- Adding linker script /mnt/D/code/hardware/blink/build/esp-idf/esp_system/ld/memory.ld
-- Adding linker script /mnt/D/code/hardware/blink/build/esp-idf/esp_system/ld/sections.ld.in
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.api.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.libgcc.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.newlib-data.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.syscalls.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.newlib-funcs.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/soc/esp32/ld/esp32.peripherals.ld
-- Components: app_trace app_update bootloader bootloader_support bt cmock console cxx driver efuse esp-tls esp_adc esp_app_format esp_bootloader_format esp_coex esp_common esp_driver_ana_cmpr esp_driver_cam esp_driver_dac esp_driver_gpio esp_driver_gptimer esp_driver_i2c esp_driver_i2s esp_driver_isp esp_driver_jpeg esp_driver_ledc esp_driver_mcpwm esp_driver_parlio esp_driver_pcnt esp_driver_ppa esp_driver_rmt esp_driver_sdio esp_driver_sdm esp_driver_sdmmc esp_driver_sdspi esp_driver_spi esp_driver_touch_sens esp_driver_tsens esp_driver_uart esp_driver_usb_serial_jtag esp_eth esp_event esp_gdbstub esp_hid esp_http_client esp_http_server esp_https_ota esp_https_server esp_hw_support esp_lcd esp_local_ctrl esp_mm esp_netif esp_netif_stack esp_partition esp_phy esp_pm esp_psram esp_ringbuf esp_rom esp_security esp_system esp_timer esp_vfs_console esp_wifi espcoredump espressif__led_strip esptool_py fatfs freertos hal heap http_parser idf_test ieee802154 json log lwip main mbedtls mqtt newlib nvs_flash nvs_sec_provider openthread partition_table perfmon protobuf-c protocomm pthread rt sdmmc soc spi_flash spiffs tcp_transport ulp unity usb vfs wear_levelling wifi_provisioning wpa_supplicant xtensa
-- Component paths: /home/dark-neonus/esp/v5.4.1/esp-idf/components/app_trace /home/dark-neonus/esp/v5.4.1/esp-idf/components/app_update /home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader /home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader_support /home/dark-neonus/esp/v5.4.1/esp-idf/components/bt /home/dark-neonus/esp/v5.4.1/esp-idf/components/cmock /home/dark-neonus/esp/v5.4.1/esp-idf/components/console /home/dark-neonus/esp/v5.4.1/esp-idf/components/cxx /home/dark-neonus/esp/v5.4.1/esp-idf/components/driver /home/dark-neonus/esp/v5.4.1/esp-idf/components/efuse /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp-tls /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_adc /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_app_format /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_bootloader_format /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_coex /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_common /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_ana_cmpr /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_cam /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_dac /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_gpio /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_gptimer /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_i2c /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_i2s /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_isp /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_jpeg /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_ledc /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_mcpwm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_parlio /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_pcnt /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_ppa /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_rmt /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdio /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdmmc /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdspi /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_spi /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_touch_sens /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_tsens /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_uart /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_usb_serial_jtag /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_eth /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_event /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_gdbstub /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_hid /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_http_client /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_http_server /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_https_ota /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_https_server /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_hw_support /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_lcd /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_local_ctrl /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_mm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_netif /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_netif_stack /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_partition /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_phy /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_pm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_psram /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_ringbuf /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_security /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_system /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_timer /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_vfs_console /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_wifi /home/dark-neonus/esp/v5.4.1/esp-idf/components/espcoredump /mnt/D/code/hardware/blink/managed_components/espressif__led_strip /home/dark-neonus/esp/v5.4.1/esp-idf/components/esptool_py /home/dark-neonus/esp/v5.4.1/esp-idf/components/fatfs /home/dark-neonus/esp/v5.4.1/esp-idf/components/freertos /home/dark-neonus/esp/v5.4.1/esp-idf/components/hal /home/dark-neonus/esp/v5.4.1/esp-idf/components/heap /home/dark-neonus/esp/v5.4.1/esp-idf/components/http_parser /home/dark-neonus/esp/v5.4.1/esp-idf/components/idf_test /home/dark-neonus/esp/v5.4.1/esp-idf/components/ieee802154 /home/dark-neonus/esp/v5.4.1/esp-idf/components/json /home/dark-neonus/esp/v5.4.1/esp-idf/components/log /home/dark-neonus/esp/v5.4.1/esp-idf/components/lwip /mnt/D/code/hardware/blink/main /home/dark-neonus/esp/v5.4.1/esp-idf/components/mbedtls /home/dark-neonus/esp/v5.4.1/esp-idf/components/mqtt /home/dark-neonus/esp/v5.4.1/esp-idf/components/newlib /home/dark-neonus/esp/v5.4.1/esp-idf/components/nvs_flash /home/dark-neonus/esp/v5.4.1/esp-idf/components/nvs_sec_provider /home/dark-neonus/esp/v5.4.1/esp-idf/components/openthread /home/dark-neonus/esp/v5.4.1/esp-idf/components/partition_table /home/dark-neonus/esp/v5.4.1/esp-idf/components/perfmon /home/dark-neonus/esp/v5.4.1/esp-idf/components/protobuf-c /home/dark-neonus/esp/v5.4.1/esp-idf/components/protocomm /home/dark-neonus/esp/v5.4.1/esp-idf/components/pthread /home/dark-neonus/esp/v5.4.1/esp-idf/components/rt /home/dark-neonus/esp/v5.4.1/esp-idf/components/sdmmc /home/dark-neonus/esp/v5.4.1/esp-idf/components/soc /home/dark-neonus/esp/v5.4.1/esp-idf/components/spi_flash /home/dark-neonus/esp/v5.4.1/esp-idf/components/spiffs /home/dark-neonus/esp/v5.4.1/esp-idf/components/tcp_transport /home/dark-neonus/esp/v5.4.1/esp-idf/components/ulp /home/dark-neonus/esp/v5.4.1/esp-idf/components/unity /home/dark-neonus/esp/v5.4.1/esp-idf/components/usb /home/dark-neonus/esp/v5.4.1/esp-idf/components/vfs /home/dark-neonus/esp/v5.4.1/esp-idf/components/wear_levelling /home/dark-neonus/esp/v5.4.1/esp-idf/components/wifi_provisioning /home/dark-neonus/esp/v5.4.1/esp-idf/components/wpa_supplicant /home/dark-neonus/esp/v5.4.1/esp-idf/components/xtensa
-- Configuring done (3.6s)
-- Generating done (0.4s)
-- Build files have been written to: /mnt/D/code/hardware/blink/build
[105/676] Performing configure step for 'bootloader'
FAILED: bootloader-prefix/src/bootloader-stamp/bootloader-configure /mnt/D/code/hardware/blink/build/bootloader-prefix/src/bootloader-stamp/bootloader-configure 
cd /mnt/D/code/hardware/blink/build/bootloader && /usr/bin/cmake -DSDKCONFIG=/mnt/D/code/hardware/blink/sdkconfig -DIDF_PATH=/home/dark-neonus/esp/v5.4.1/esp-idf -DIDF_TARGET=esp32 -DPYTHON_DEPS_CHECKED=1 -DPYTHON=/home/dark-neonus/.espressif/python_env/idf5.4_py3.11_env/bin/python -DEXTRA_COMPONENT_DIRS=/home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader -DPROJECT_SOURCE_DIR=/mnt/D/code/hardware/blink -DIGNORE_EXTRA_COMPONENT= -GNinja -S /home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader/subproject -B /mnt/D/code/hardware/blink/build/bootloader && /usr/bin/cmake -E touch /mnt/D/code/hardware/blink/build/bootloader-prefix/src/bootloader-stamp/bootloader-configure
-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- The ASM compiler identification is GNU
-- Found assembler: /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - failed
-- Check for working C compiler: /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc
-- Check for working C compiler: /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc - broken
CMake Error at /usr/share/cmake-3.28/Modules/CMakeTestCCompiler.cmake:67 (message):
  The C compiler

    "/home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc"

  is not able to compile a simple test program.

  It fails with the following output:

    Change Dir: '/mnt/D/code/hardware/blink/build/bootloader/CMakeFiles/CMakeScratch/TryCompile-P7O1UZ'
    
    Run Build Command(s): /usr/bin/ninja -v cmTC_b92d2
    [1/2] /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc   -mlongcalls -Wno-frame-address  -fno-builtin-memcpy -fno-builtin-memset -fno-builtin-bzero -fno-builtin-stpcpy -fno-builtin-strncpy -o CMakeFiles/cmTC_b92d2.dir/testCCompiler.c.obj -c /mnt/D/code/hardware/blink/build/bootloader/CMakeFiles/CMakeScratch/TryCompile-P7O1UZ/testCCompiler.c
    [2/2] : && /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc -mlongcalls -Wno-frame-address  -fno-builtin-memcpy -fno-builtin-memset -fno-builtin-bzero -fno-builtin-stpcpy -fno-builtin-strncpy  CMakeFiles/cmTC_b92d2.dir/testCCompiler.c.obj -o cmTC_b92d2   && :
    FAILED: cmTC_b92d2 
    : && /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc -mlongcalls -Wno-frame-address  -fno-builtin-memcpy -fno-builtin-memset -fno-builtin-bzero -fno-builtin-stpcpy -fno-builtin-strncpy  CMakeFiles/cmTC_b92d2.dir/testCCompiler.c.obj -o cmTC_b92d2   && :
    /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/../lib/gcc/xtensa-esp-elf/14.2.0/../../../../xtensa-esp-elf/bin/ld: cannot find -lc: No such file or directory
    /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/../lib/gcc/xtensa-esp-elf/14.2.0/../../../../xtensa-esp-elf/bin/ld: cannot find -lnosys: No such file or directory
    /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/../lib/gcc/xtensa-esp-elf/14.2.0/../../../../xtensa-esp-elf/bin/ld: cannot find -lc: No such file or directory
    collect2: error: ld returned 1 exit status
    ninja: build stopped: subcommand failed.
    
    

  

  CMake will not be able to correctly generate this project.
Call Stack (most recent call first):
  /home/dark-neonus/esp/v5.4.1/esp-idf/tools/cmake/project.cmake:571 (__project)
  CMakeLists.txt:67 (project)


-- Configuring incomplete, errors occurred!
[118/676] Building CXX object esp-idf/nvs_flash/CMa...idf_nvs_flash.dir/src/nvs_partition_manager.cpp.obj
ninja: build stopped: subcommand failed.

 *  The terminal process "ninja" terminated with exit code: 1. 
```

About this i found [this problem on Stack Overflow](https://stackoverflow.com/questions/53633705/cmake-the-c-compiler-is-not-able-to-compile-a-simple-test-program)

Ans as it suggested I have added
```CMake
set(CMAKE_TRY_COMPILE_TARGET_TYPE "STATIC_LIBRARY")
```
To `blink\CMakeLists.txt`

Now i get the same fucking error message.
Tried to put same line insode `managed_components/espressif__led_strip/CMakeLists.txt` didnt help. Remove it from there after try. Same with `main/CMakeLists.txt`

... (bla bla bla, nothing works her)
I checked version if esp idf and it's looking suspicious `ESP-IDF v5.4.1-dirty`.
Chat GRT do shit, but also recoomned to do something with git inside esp idf directory.
I have navigated there and run there:
```bash
git reset --hard
git clean -fd
```
Now will try to clean and build. (Fuck, still have `-dirty` version). Nothing changed, same error.
Tried: `python /home/dark-neonus/esp/v5.4.1/esp-idf/tools/idf_tools.py uninstall` didnt helped.
Okay, I am stupid a little bit. I forgot to remove this two lines i pasted in `blink/CMakeLists.txt`:
```CmakeLists
SET (CMAKE_C_COMPILER_WORKS 1)
SET (CMAKE_CXX_COMPILER_WORKS 1)
```
Now i have slightly different error(it occur in build step 324/1002 instead of 307/1002)

As ChatAGPT suggested, i inited git repo inside blink directory. Nwo i get slightly different erro, but now at step 316/1002.

Changed python environment path from ros to esp idf, no great changes:
`[323/1002] Performing configure step for 'bootloader'`(Spoiler: everything was okay, nothing changed)

Copilot suggested me to try install command once again and I am giving up on this installing error:
```sh
(base) dark-neonus@NeonMachine:/mnt/D/code/hardware/blink$ idf.py install
Executing action: install
Running cmake in directory /mnt/D/code/hardware/blink/build
Executing "cmake -G Ninja -DPYTHON_DEPS_CHECKED=1 -DPYTHON=/home/dark-neonus/.espressif/python_env/idf5.4_py3.11_env/bin/python -DESP_PLATFORM=1 -DCCACHE_ENABLE=0 /mnt/D/code/hardware/blink"...
-- Building ESP-IDF components for target esp32
NOTICE: Processing 2 dependencies:
NOTICE: [1/2] espressif/led_strip (2.5.5)
NOTICE: [2/2] idf (5.4.1)
-- Project sdkconfig file /mnt/D/code/hardware/blink/sdkconfig
Loading defaults file /mnt/D/code/hardware/blink/sdkconfig.defaults...
Loading defaults file /mnt/D/code/hardware/blink/sdkconfig.defaults.esp32...
-- Compiler supported targets: xtensa-esp-elf
-- App "blink" version: 03a4a36-dirty
-- Adding linker script /mnt/D/code/hardware/blink/build/esp-idf/esp_system/ld/memory.ld
-- Adding linker script /mnt/D/code/hardware/blink/build/esp-idf/esp_system/ld/sections.ld.in
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.api.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.libgcc.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.newlib-data.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.syscalls.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom/esp32/ld/esp32.rom.newlib-funcs.ld
-- Adding linker script /home/dark-neonus/esp/v5.4.1/esp-idf/components/soc/esp32/ld/esp32.peripherals.ld
-- Components: app_trace app_update bootloader bootloader_support bt cmock console cxx driver efuse esp-tls esp_adc esp_app_format esp_bootloader_format esp_coex esp_common esp_driver_ana_cmpr esp_driver_cam esp_driver_dac esp_driver_gpio esp_driver_gptimer esp_driver_i2c esp_driver_i2s esp_driver_isp esp_driver_jpeg esp_driver_ledc esp_driver_mcpwm esp_driver_parlio esp_driver_pcnt esp_driver_ppa esp_driver_rmt esp_driver_sdio esp_driver_sdm esp_driver_sdmmc esp_driver_sdspi esp_driver_spi esp_driver_touch_sens esp_driver_tsens esp_driver_uart esp_driver_usb_serial_jtag esp_eth esp_event esp_gdbstub esp_hid esp_http_client esp_http_server esp_https_ota esp_https_server esp_hw_support esp_lcd esp_local_ctrl esp_mm esp_netif esp_netif_stack esp_partition esp_phy esp_pm esp_psram esp_ringbuf esp_rom esp_security esp_system esp_timer esp_vfs_console esp_wifi espcoredump espressif__led_strip esptool_py fatfs freertos hal heap http_parser idf_test ieee802154 json log lwip main mbedtls mqtt newlib nvs_flash nvs_sec_provider openthread partition_table perfmon protobuf-c protocomm pthread rt sdmmc soc spi_flash spiffs tcp_transport ulp unity usb vfs wear_levelling wifi_provisioning wpa_supplicant xtensa
-- Component paths: /home/dark-neonus/esp/v5.4.1/esp-idf/components/app_trace /home/dark-neonus/esp/v5.4.1/esp-idf/components/app_update /home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader /home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader_support /home/dark-neonus/esp/v5.4.1/esp-idf/components/bt /home/dark-neonus/esp/v5.4.1/esp-idf/components/cmock /home/dark-neonus/esp/v5.4.1/esp-idf/components/console /home/dark-neonus/esp/v5.4.1/esp-idf/components/cxx /home/dark-neonus/esp/v5.4.1/esp-idf/components/driver /home/dark-neonus/esp/v5.4.1/esp-idf/components/efuse /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp-tls /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_adc /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_app_format /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_bootloader_format /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_coex /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_common /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_ana_cmpr /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_cam /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_dac /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_gpio /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_gptimer /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_i2c /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_i2s /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_isp /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_jpeg /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_ledc /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_mcpwm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_parlio /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_pcnt /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_ppa /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_rmt /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdio /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdmmc /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_sdspi /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_spi /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_touch_sens /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_tsens /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_uart /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_driver_usb_serial_jtag /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_eth /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_event /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_gdbstub /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_hid /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_http_client /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_http_server /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_https_ota /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_https_server /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_hw_support /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_lcd /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_local_ctrl /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_mm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_netif /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_netif_stack /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_partition /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_phy /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_pm /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_psram /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_ringbuf /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_rom /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_security /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_system /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_timer /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_vfs_console /home/dark-neonus/esp/v5.4.1/esp-idf/components/esp_wifi /home/dark-neonus/esp/v5.4.1/esp-idf/components/espcoredump /mnt/D/code/hardware/blink/managed_components/espressif__led_strip /home/dark-neonus/esp/v5.4.1/esp-idf/components/esptool_py /home/dark-neonus/esp/v5.4.1/esp-idf/components/fatfs /home/dark-neonus/esp/v5.4.1/esp-idf/components/freertos /home/dark-neonus/esp/v5.4.1/esp-idf/components/hal /home/dark-neonus/esp/v5.4.1/esp-idf/components/heap /home/dark-neonus/esp/v5.4.1/esp-idf/components/http_parser /home/dark-neonus/esp/v5.4.1/esp-idf/components/idf_test /home/dark-neonus/esp/v5.4.1/esp-idf/components/ieee802154 /home/dark-neonus/esp/v5.4.1/esp-idf/components/json /home/dark-neonus/esp/v5.4.1/esp-idf/components/log /home/dark-neonus/esp/v5.4.1/esp-idf/components/lwip /mnt/D/code/hardware/blink/main /home/dark-neonus/esp/v5.4.1/esp-idf/components/mbedtls /home/dark-neonus/esp/v5.4.1/esp-idf/components/mqtt /home/dark-neonus/esp/v5.4.1/esp-idf/components/newlib /home/dark-neonus/esp/v5.4.1/esp-idf/components/nvs_flash /home/dark-neonus/esp/v5.4.1/esp-idf/components/nvs_sec_provider /home/dark-neonus/esp/v5.4.1/esp-idf/components/openthread /home/dark-neonus/esp/v5.4.1/esp-idf/components/partition_table /home/dark-neonus/esp/v5.4.1/esp-idf/components/perfmon /home/dark-neonus/esp/v5.4.1/esp-idf/components/protobuf-c /home/dark-neonus/esp/v5.4.1/esp-idf/components/protocomm /home/dark-neonus/esp/v5.4.1/esp-idf/components/pthread /home/dark-neonus/esp/v5.4.1/esp-idf/components/rt /home/dark-neonus/esp/v5.4.1/esp-idf/components/sdmmc /home/dark-neonus/esp/v5.4.1/esp-idf/components/soc /home/dark-neonus/esp/v5.4.1/esp-idf/components/spi_flash /home/dark-neonus/esp/v5.4.1/esp-idf/components/spiffs /home/dark-neonus/esp/v5.4.1/esp-idf/components/tcp_transport /home/dark-neonus/esp/v5.4.1/esp-idf/components/ulp /home/dark-neonus/esp/v5.4.1/esp-idf/components/unity /home/dark-neonus/esp/v5.4.1/esp-idf/components/usb /home/dark-neonus/esp/v5.4.1/esp-idf/components/vfs /home/dark-neonus/esp/v5.4.1/esp-idf/components/wear_levelling /home/dark-neonus/esp/v5.4.1/esp-idf/components/wifi_provisioning /home/dark-neonus/esp/v5.4.1/esp-idf/components/wpa_supplicant /home/dark-neonus/esp/v5.4.1/esp-idf/components/xtensa
-- Configuring done (3.9s)
-- Generating done (0.5s)
-- Build files have been written to: /mnt/D/code/hardware/blink/build
Running ninja in directory /mnt/D/code/hardware/blink/build
Executing "ninja install"...
[1/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/dac_periph.c.obj
[2/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/touch_sensor_periph.c.obj
[3/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/twai_periph.c.obj
[4/683] Building C object esp-idf/esp_security/CMakeFiles/__idf_esp_security.dir/src/esp_crypto_lock.c.obj
[5/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/wdt_periph.c.obj
[6/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/sdmmc_periph.c.obj
[7/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/sdio_slave_periph.c.obj
[8/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/esp_memory_utils.c.obj
[9/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/esp_cpu_intr.c.obj
[10/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/cpu_region_protect.c.obj
[11/683] Building C object esp-idf/soc/CMakeFiles/__idf_soc.dir/esp32/rtc_io_periph.c.obj
[12/683] Building C object esp-idf/esp_security/CMakeFiles/__idf_esp_security.dir/src/init.c.obj
[13/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/revision.c.obj
[14/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/cpu.c.obj
[15/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_console.c.obj
[16/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_usb.c.obj
[17/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/hw_random.c.obj
[18/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/mac_addr.c.obj
[19/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/clk_ctrl_os.c.obj
[20/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/esp_gpio_reserve.c.obj
[21/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/esp_clk.c.obj
[22/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_modem.c.obj
[23/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sar_periph_ctrl_common.c.obj
[24/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_event.c.obj
[25/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/io_mux.c.obj
[26/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/periph_ctrl.c.obj
[27/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/rtc_module.c.obj
[28/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/regi2c_ctrl.c.obj
[29/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_gpio.c.obj
[30/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp_clk_tree_common.c.obj
[31/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/clk_utils.c.obj
[32/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/rtc_wdt.c.obj
[33/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/intr_alloc.c.obj
[34/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/mspi_timing_tuning.c.obj
[35/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/dma/esp_dma_utils.c.obj
[36/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/esp_clk_tree.c.obj
[37/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/spi_share_hw_ctrl.c.obj
[38/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/spi_bus_lock.c.obj
[39/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/dma/gdma_link.c.obj
[40/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/adc_share_hw_ctrl.c.obj
[41/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/cache_sram_mmu.c.obj
[42/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/chip_info.c.obj
[43/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/sar_periph_ctrl.c.obj
[44/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_wake_stub.c.obj
[45/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/port_common.c.obj
[46/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/app_startup.c.obj
[47/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/esp_clock_output.c.obj
[48/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/heap_idf.c.obj
[49/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/rtc_init.c.obj
[50/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/rtc_clk_init.c.obj
[51/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/rtc_sleep.c.obj
[52/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/rtc_time.c.obj
[53/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/sleep_modes.c.obj
[54/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/port_systick.c.obj
[55/683] Building ASM object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/portable/xtensa/portasm.S.obj
[56/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/list.c.obj
[57/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/portable/xtensa/xtensa_init.c.obj
[58/683] Building C object esp-idf/esp_hw_support/CMakeFiles/__idf_esp_hw_support.dir/port/esp32/rtc_clk.c.obj
[59/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/esp_additions/idf_additions_event_groups.c.obj
[60/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/event_groups.c.obj
[61/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/portable/xtensa/xtensa_overlay_os_hook.c.obj
[62/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/esp_additions/freertos_compatibility.c.obj
[63/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/abort.c.obj
[64/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/assert.c.obj
[65/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/timers.c.obj
[66/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/flockfile.c.obj
[67/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/pthread.c.obj
[68/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/heap.c.obj
[69/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/random.c.obj
[70/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/portable/xtensa/port.c.obj
[71/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/getentropy.c.obj
[72/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/reent_init.c.obj
[73/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/poll.c.obj
[74/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/stream_buffer.c.obj
[75/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/esp_additions/idf_additions.c.obj
[76/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/termios.c.obj
[77/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/queue.c.obj
[78/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/locks.c.obj
[79/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/newlib_init.c.obj
[80/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/scandir.c.obj
[81/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/syscalls.c.obj
[82/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/realpath.c.obj
[83/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/port/esp_time_impl.c.obj
[84/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/sysconf.c.obj
[85/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/time.c.obj
[86/683] Building C object esp-idf/pthread/CMakeFiles/__idf_pthread.dir/pthread_cond_var.c.obj
[87/683] Building CXX object esp-idf/cxx/CMakeFiles/__idf_cxx.dir/cxx_init.cpp.obj
[88/683] Building C object esp-idf/newlib/CMakeFiles/__idf_newlib.dir/stdatomic.c.obj
[89/683] Building C object esp-idf/esp_timer/CMakeFiles/__idf_esp_timer.dir/src/esp_timer_init.c.obj
[90/683] Building C object esp-idf/pthread/CMakeFiles/__idf_pthread.dir/pthread_semaphore.c.obj
[91/683] Building CXX object esp-idf/cxx/CMakeFiles/__idf_cxx.dir/cxx_exception_stubs.cpp.obj
[92/683] Building C object esp-idf/pthread/CMakeFiles/__idf_pthread.dir/pthread_local_storage.c.obj
[93/683] Building C object esp-idf/pthread/CMakeFiles/__idf_pthread.dir/pthread_rwlock.c.obj
[94/683] Building C object esp-idf/esp_timer/CMakeFiles/__idf_esp_timer.dir/src/system_time.c.obj
[95/683] Building C object esp-idf/esp_timer/CMakeFiles/__idf_esp_timer.dir/src/esp_timer_impl_common.c.obj
[96/683] Building C object esp-idf/esp_timer/CMakeFiles/__idf_esp_timer.dir/src/ets_timer_legacy.c.obj
[97/683] Building C object esp-idf/pthread/CMakeFiles/__idf_pthread.dir/pthread.c.obj
[98/683] Building C object esp-idf/esp_timer/CMakeFiles/__idf_esp_timer.dir/src/esp_timer.c.obj
[99/683] Building C object esp-idf/esp_event/CMakeFiles/__idf_esp_event.dir/default_event_loop.c.obj
[100/683] Building C object esp-idf/esp_timer/CMakeFiles/__idf_esp_timer.dir/src/esp_timer_impl_lac.c.obj
[101/683] Building C object esp-idf/esp_driver_gptimer/CMakeFiles/__idf_esp_driver_gptimer.dir/src/gptimer_common.c.obj
[102/683] Building C object esp-idf/freertos/CMakeFiles/__idf_freertos.dir/FreeRTOS-Kernel/tasks.c.obj
[103/683] Building C object esp-idf/esp_event/CMakeFiles/__idf_esp_event.dir/esp_event_private.c.obj
[104/683] Building C object esp-idf/esp_driver_gptimer/CMakeFiles/__idf_esp_driver_gptimer.dir/src/gptimer.c.obj
[105/683] Building C object esp-idf/esp_driver_uart/CMakeFiles/__idf_esp_driver_uart.dir/src/uart_vfs.c.obj
[106/683] Building C object esp-idf/esp_event/CMakeFiles/__idf_esp_event.dir/esp_event.c.obj
[107/683] Building C object esp-idf/esp_ringbuf/CMakeFiles/__idf_esp_ringbuf.dir/ringbuf.c.obj
[108/683] Building CXX object esp-idf/cxx/CMakeFiles/__idf_cxx.dir/cxx_guards.cpp.obj
[109/683] Performing configure step for 'bootloader'
FAILED: bootloader-prefix/src/bootloader-stamp/bootloader-configure /mnt/D/code/hardware/blink/build/bootloader-prefix/src/bootloader-stamp/bootloader-configure 
cd /mnt/D/code/hardware/blink/build/bootloader && /usr/bin/cmake -DSDKCONFIG=/mnt/D/code/hardware/blink/sdkconfig -DIDF_PATH=/home/dark-neonus/esp/v5.4.1/esp-idf -DIDF_TARGET=esp32 -DPYTHON_DEPS_CHECKED=1 -DPYTHON=/home/dark-neonus/.espressif/python_env/idf5.4_py3.11_env/bin/python -DEXTRA_COMPONENT_DIRS=/home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader -DPROJECT_SOURCE_DIR=/mnt/D/code/hardware/blink -DIGNORE_EXTRA_COMPONENT= -GNinja -S /home/dark-neonus/esp/v5.4.1/esp-idf/components/bootloader/subproject -B /mnt/D/code/hardware/blink/build/bootloader && /usr/bin/cmake -E touch /mnt/D/code/hardware/blink/build/bootloader-prefix/src/bootloader-stamp/bootloader-configure
-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- The ASM compiler identification is GNU
-- Found assembler: /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - failed
-- Check for working C compiler: /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc
-- Check for working C compiler: /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc - broken
CMake Error at /usr/share/cmake-3.28/Modules/CMakeTestCCompiler.cmake:67 (message):
  The C compiler

    "/home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc"

  is not able to compile a simple test program.

  It fails with the following output:

    Change Dir: '/mnt/D/code/hardware/blink/build/bootloader/CMakeFiles/CMakeScratch/TryCompile-uv71mH'
    
    Run Build Command(s): /usr/bin/ninja -v cmTC_e75e2
    [1/2] /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc   -mlongcalls -Wno-frame-address  -fno-builtin-memcpy -fno-builtin-memset -fno-builtin-bzero -fno-builtin-stpcpy -fno-builtin-strncpy -o CMakeFiles/cmTC_e75e2.dir/testCCompiler.c.obj -c /mnt/D/code/hardware/blink/build/bootloader/CMakeFiles/CMakeScratch/TryCompile-uv71mH/testCCompiler.c
    [2/2] : && /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc -mlongcalls -Wno-frame-address  -fno-builtin-memcpy -fno-builtin-memset -fno-builtin-bzero -fno-builtin-stpcpy -fno-builtin-strncpy  CMakeFiles/cmTC_e75e2.dir/testCCompiler.c.obj -o cmTC_e75e2   && :
    FAILED: cmTC_e75e2 
    : && /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/xtensa-esp32-elf-gcc -mlongcalls -Wno-frame-address  -fno-builtin-memcpy -fno-builtin-memset -fno-builtin-bzero -fno-builtin-stpcpy -fno-builtin-strncpy  CMakeFiles/cmTC_e75e2.dir/testCCompiler.c.obj -o cmTC_e75e2   && :
    /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/../lib/gcc/xtensa-esp-elf/14.2.0/../../../../xtensa-esp-elf/bin/ld: cannot find -lc: No such file or directory
    /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/../lib/gcc/xtensa-esp-elf/14.2.0/../../../../xtensa-esp-elf/bin/ld: cannot find -lnosys: No such file or directory
    /home/dark-neonus/.espressif/tools/xtensa-esp-elf/esp-14.2.0_20241119/xtensa-esp-elf/bin/../lib/gcc/xtensa-esp-elf/14.2.0/../../../../xtensa-esp-elf/bin/ld: cannot find -lc: No such file or directory
    collect2: error: ld returned 1 exit status
    ninja: build stopped: subcommand failed.
    
    

  

  CMake will not be able to correctly generate this project.
Call Stack (most recent call first):
  /home/dark-neonus/esp/v5.4.1/esp-idf/tools/cmake/project.cmake:571 (__project)
  CMakeLists.txt:67 (project)


-- Configuring incomplete, errors occurred!
[110/683] Building C object esp-idf/esp_driver_uart/CMakeFiles/__idf_esp_driver_uart.dir/src/uart.c.obj
[111/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_partition.cpp.obj
[112/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_partition_lookup.cpp.obj
[113/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_item_hash_list.cpp.obj
[114/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_handle_simple.cpp.obj
[115/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_handle_locked.cpp.obj
[116/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_pagemanager.cpp.obj
[117/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_page.cpp.obj
[118/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_types.cpp.obj
[119/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_cxx_api.cpp.obj
[120/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_partition_manager.cpp.obj
[121/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_storage.cpp.obj
[122/683] Building CXX object esp-idf/nvs_flash/CMakeFiles/__idf_nvs_flash.dir/src/nvs_api.cpp.obj
ninja: build stopped: subcommand failed.
ninja failed with exit code 1, output of the command is in the /mnt/D/code/hardware/blink/build/log/idf_py_stderr_output_74893 and /mnt/D/code/hardware/blink/build/log/idf_py_stdout_output_74893
```


