include_directories (
  ../../core/include
)

add_library (
  mod_file
  ${MODULES}
  mod_file.c
) 

target_link_libraries (
  mod_file
  bgdrtm
)

if (NOT STATIC_MODULES)
  install (
    TARGETS
    mod_file
    DESTINATION
    /usr/lib
  )
endif ()
