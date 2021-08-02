set(COMPONENT_ADD_INCLUDEDIRS ./include)


# Edit following two lines to set component requirements (see docs)
set(COMPONENT_REQUIRES )
set(COMPONENT_PRIV_REQUIRES )

set(COMPONENT_SRCS )

register_component()


target_link_libraries(${COMPONENT_TARGET} INTERFACE "-Wl,--start-group"
	libesp_sip.a "-Wl,--end-group")