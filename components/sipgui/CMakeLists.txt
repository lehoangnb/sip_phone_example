set(COMPONENT_ADD_INCLUDEDIRS .  .. ../)

# Edit following two lines to set component requirements (see docs)
set(COMPONENT_REQUIRES )
set(COMPONENT_PRIV_REQUIRES lvgl esp_sip audio_board)

set(COMPONENT_SRCS ./gui.c ./img_bubble_pattern.c)

register_component()
component_compile_options(-DLV_CONF_INCLUDE_SIMPLE)
