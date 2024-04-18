zephyr_include_directories( # global includes
	src
)

add_library(SWDR001 INTERFACE)
target_link_libraries(SWDR001 INTERFACE zephyr_interface)
zephyr_library()
zephyr_library_sources(
	src/lr11xx_radio.c
	src/lr11xx_regmem.c
	src/lr11xx_system.c
	src/lr11xx_lr_fhss.c
	src/lr11xx_bootloader.c
	src/lr11xx_crypto_engine.c
	src/lr11xx_driver_version.c
	src/lr11xx_gnss.c
	src/lr11xx_radio_timings.c
	src/lr11xx_wifi.c
)
