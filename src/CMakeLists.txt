file(GLOB SOURCES *.c)
file(GLOB HEADERS *.h)

add_library(rnnoise ${SOURCES} ${HEADERS})

if (MSVC)
    target_compile_definitions(rnnoise PRIVATE "USE_MALLOC")
endif()
