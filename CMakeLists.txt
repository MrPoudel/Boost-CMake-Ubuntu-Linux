#CMakeLists.txt
cmake_minimum_required (VERSION 3.7)
project (Boost_program_option_example)

#Set default build type

if(NOT CMAKE_BUILD_TYPE)
    message(STATUS "CMAKE_BUILD_TYPE not given; setting to 'Debug'")
    set(CMAKE_BUILD_TYPE "Debug" CACHE STRING "Choose the type of build" FORCE)
endif()

#main project set up
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

#Boost related setup

#set(Boost_INCLUDE_DIR /usr/include/)
#set(Boost_LIBRARY_DIR /usr/lib/)

find_package(Boost 1.65.1 REQUIRED COMPONENTS program_options)
include_directories(${Boost_INCLUDE_DIR})
link_directories(${Boost_LIBRARY_DIR})

option(ENABLE_EXAMPLES "Building the examples" OFF)

if(Boost_FOUND)
	include_directories(${Boost_INCLUDE_DIR})
	#ADD_DEFINITIONS("-DHAS_BOOST")

        #Just for debugging purpose
	message(${Boost_INCLUDE_DIR})	

	if(ENABLE_EXAMPLES)

    #header only files doesnot need to be included
	add_executable(header_only examples/header_only.cpp)
	
	add_executable(boost_program_option examples/boost_program_option.cpp)
    target_link_libraries(boost_program_option ${Boost_LIBRARIES})
	
	endif()

endif()
