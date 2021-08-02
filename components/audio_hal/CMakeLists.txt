set(COMPONENT_ADD_INCLUDEDIRS . ./include ./driver/es8388)

set(COMPONENT_PRIV_INCLUDEDIRS ./driver/include)


# Edit following two lines to set component requirements (see docs)
set(COMPONENT_REQUIRES )
set(COMPONENT_PRIV_REQUIRES esp_peripherals audio_sal audio_board)

set(COMPONENT_SRCS ./audio_hal.c ./driver/es8388/headphone_detect.c ./driver/es8388/es8388.c)

register_component()
