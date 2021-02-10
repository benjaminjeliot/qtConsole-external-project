# Copyright 2021 Jim Eliot

cmake_minimum_required(VERSION 3.16)

project("qtconsole-external-project")

option(Python_enabled "Build with a console using Python and Numpy" ON)

if(Python_enabled)
  add_subdirectory(qtConsole)
  find_package(Python3 COMPONENTS Interpreter Development NumPy REQUIRED)
endif()
