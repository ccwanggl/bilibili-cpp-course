cmake_minimum_required(VERSION 3.12)

set(CMAKE_CXX_STANDARD 20)

project(main)

add_compile_options(-Wall -Wextra -Wreturn-type)

file(GLOB sources CONFIGURE_DEPENDS "*.cpp")
foreach(source IN LISTS sources)
    get_filename_component(name ${source} NAME_WE)
    add_executable(${name} ${source})
endforeach()
