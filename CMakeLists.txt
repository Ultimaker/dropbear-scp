project(dropbear-scp)

cmake_minimum_required(VERSION 2.8.12)

# Add warnings
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

set(SOURCES scp.c progressmeter.c compat.c scpmisc.c atomicio.c)

add_executable(scp ${SOURCES})

include(CPackConfig.cmake)

include(GNUInstallDirs)
install(TARGETS scp DESTINATION ${CMAKE_INSTALL_BINDIR})
