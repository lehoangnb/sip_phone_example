set(COMPONENT_ADD_INCLUDEDIRS .  .. ../)

# Edit following two lines to set component requirements (see docs)
set(COMPONENT_REQUIRES )
set(COMPONENT_PRIV_REQUIRES audio_board lvgl)

set(COMPONENT_SRCS ./disp_spi.c ./stmpe610.c ./ili9341.c)

register_component()
component_compile_options(-DLV_CONF_INCLUDE_SIMPLE -DILI9341_BCKL_ACTIVE_LVL=0 -DTOUCH_SUPPORT=1 -LV_USE_ANIMATION=1)
