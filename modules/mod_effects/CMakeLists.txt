include_directories (
  ../../core/include
  ../libgrbase
)

add_library (
  mod_effects
  ${MODULES}
  mod_effects.c
) 

target_link_libraries (
  mod_effects
  grbase
)

if (NOT STATIC_MODULES)
  install (
    TARGETS
    mod_effects
    DESTINATION
    /usr/lib
  )
endif ()
