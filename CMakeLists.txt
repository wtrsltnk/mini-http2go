cmake_minimum_required(VERSION 3.3)

project(mini-http2go)

add_executable(mini-http2go
    server.cpp
)

target_compile_features(mini-http2go
    PRIVATE cxx_auto_type
    PRIVATE cxx_nullptr
    PRIVATE cxx_range_for
    PRIVATE cxx_thread_local
)

target_link_libraries(mini-http2go
    ws2_32
)

target_compile_definitions(mini-http2go
    PUBLIC -DWIN32
)
