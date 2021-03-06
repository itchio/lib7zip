cmake_minimum_required(VERSION 2.8)

project(test7zip)

set(SRC ${CMAKE_CURRENT_SOURCE_DIR})

set(test7zip_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7Zip.cpp
)

set(test7zip2_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7Zip.cpp
)

set(test7zipmulti_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7ZipMulti.cpp
)

set(test7zprops_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/test7ziprops.cpp
)

set(test7zcrypt_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7ZipCryptFileName.cpp
)

set(test7zipsig_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7ZipSignature.cpp
)

set(test7ziprar5_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7ZipRar5.cpp
)

set(test7zipcallback_SOURCES
  ${SRC}/stdafx.cpp
  ${SRC}/Test7ZipCallback.cpp
)

add_executable(test7zip ${test7zip_SOURCES})
target_link_libraries(test7zip 7zip)
target_compile_options(test7zip PRIVATE -std=c++11)

add_executable(test7zip2 ${test7zip_SOURCES})
target_link_libraries(test7zip2 7zip)
target_compile_options(test7zip2 PRIVATE -std=c++11)

add_executable(test7zipmulti ${test7zipmulti_SOURCES})
target_link_libraries(test7zipmulti 7zip)
target_compile_options(test7zipmulti PRIVATE -std=c++11)

add_executable(test7zcrypt ${test7zcrypt_SOURCES})
target_link_libraries(test7zcrypt 7zip)
target_compile_options(test7zcrypt PRIVATE -std=c++11)

add_executable(test7zipsig ${test7zipsig_SOURCES})
target_link_libraries(test7zipsig 7zip)
target_compile_options(test7zipsig PRIVATE -std=c++11)

add_executable(test7ziprar5 ${test7ziprar5_SOURCES})
target_link_libraries(test7ziprar5 7zip)
target_compile_options(test7ziprar5 PRIVATE -std=c++11)

add_executable(test7zipcallback ${test7zipcallback_SOURCES})
target_link_libraries(test7zipcallback 7zip)
target_compile_options(test7zipcallback PRIVATE -std=c++11)

configure_file(${SRC}/Test7Zip.7z ${CMAKE_CURRENT_BINARY_DIR}/Test7Zip.7z COPYONLY)
configure_file(${SRC}/Test7Zip.zip ${CMAKE_CURRENT_BINARY_DIR}/Test7Zip.zip COPYONLY)
configure_file(${SRC}/Test7ZipCryptFileName.7z ${CMAKE_CURRENT_BINARY_DIR}/Test7ZipCryptFileName.7z COPYONLY)
configure_file(${SRC}/TestRar5.rar ${CMAKE_CURRENT_BINARY_DIR}/TestRar5.rar COPYONLY)

