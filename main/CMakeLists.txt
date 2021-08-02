set(COMPONENT_ADD_INCLUDEDIRS )

# Edit following two lines to set component requirements (see docs)
set(COMPONENT_REQUIRES )
set(COMPONENT_PRIV_REQUIRES )

set(COMPONENT_SRCS ./voip_app.c)
set(COMPONENT_EMBED_TXTFILES adf_music.mp3)

register_component()