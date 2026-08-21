cmake_minimum_required(VERSION 3.20)

project(cpp_habilis VERSION 0.1.0 LANGUAGES CXX)

add_executable(cpp_habilis
	src/main.cpp
)

# Apply cmake mapping of C++ language features to compiler specific arguments
# cpp_habilis: Most warnings + warnings as errors
# Also see: https://github.com/cpp-best-practices/cppbestpractices/blob/master/02-Use_the_Tools_Available.md
target_compile_features(cpp_habilis PRIVATE cxx_std_23)

# Adapt compiler otpions to concrete compiler
if(MSVC)
	target_compile_options(cpp_habilis PRIVATE
    /W4
    /w14640
    /permissive-
  )
else()
	target_compile_options(cpp_habilis PRIVATE
    -Wall 
    -Wextra 
    -Wshadow 
    -Wnon-virtual-dtor 
    -pedantic
  )
endif()

# Use the cmake support for cross platform install folders structure and location
# Note: 'Gnu' Naming is a bit confusing?
include(GNUInstallDirs)

# Define what cmake install should do
install(TARGETS cpp_habilis
	RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
