# Устанавливаем минимальную версию CMake 3.4
cmake_minimum_required(VERSION 3.4)

# Устанавливаем версию стандарта C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED 11)

# Указываем название проекта
project(formatter_lib)

# Подключаем файл `formatter.cpp`, как статическую библиотеку
# Явно подключать файл `formatter.h` не обязательно
add_library(formatter_lib STATIC ${CMAKE_HOME_DIRECTORY}/formatter.cpp)

# Указываем директорию для подключения
target_include_directories(formatter_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
