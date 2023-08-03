cmake_minimum_required(VERSION 3.20)
project(vsg_conan_example)

#add cmake script to downlad conan-cmake integrations
include(.cmake/conan_config.cmake)

conan_cmake_autodetect(settings)
conan_cmake_install(PATH_OR_REFERENCE .
                    BUILD missing
                    REMOTE conancenter
				    SETTINGS ${settings})


find_package(vsg CONFIG REQUIRED)

add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME} 
	PRIVATE 
		vsg::vsg
)
