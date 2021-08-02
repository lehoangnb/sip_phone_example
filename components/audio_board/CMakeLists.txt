set(COMPONENT_ADD_INCLUDEDIRS ./include)

# Edit following two lines to set component requirements (see docs)
set(COMPONENT_REQUIRES )
set(COMPONENT_PRIV_REQUIRES audio_hal audio_sal esp_peripherals)

if (CONFIG_ESP32_ADF_REVB_BOARD)
message(STATUS "Current board name is " CONFIG_ESP32_ADF_REVB_BOARD)
list(APPEND COMPONENT_ADD_INCLUDEDIRS ./olimex_esp32_adf_b)
set(COMPONENT_SRCS
./olimex_esp32_adf_b/board.c
./olimex_esp32_adf_b/board_pins_config.c
)
endif()

if (CONFIG_ESP32_ADF_REVC_BOARD)
message(STATUS "Current board name is " CONFIG_ESP32_ADF_REVC_BOARD)
list(APPEND COMPONENT_ADD_INCLUDEDIRS ./olimex_esp32_adf_c)
set(COMPONENT_SRCS
./olimex_esp32_adf_c/board.c
./olimex_esp32_adf_c/board_pins_config.c
)
endif()

register_component()
