cmake_minimum_required (VERSION 2.8)
project (Kernel-Borg C ASM)
enable_language(ASM_NASM)

set(CMAKE_ASM_NASM_FLAGS "${CMAKE_ASM_NASM_FLAGS} -f bin")

#set_source_files_properties(${CMAKE_CURRENT_SOURCE_DIR}/src/boot/boot.asm PROPERTIES COMPILE_FLAGS "-x assembler-with-cpp")
add_executable(kernel "${CMAKE_CURRENT_SOURCE_DIR}/src/boot/boot.asm" "${CMAKE_CURRENT_SOURCE_DIR}/src/kmain.cpp")
#SET_TARGET_PROPERTIES(kernel PROPERTIES LINK_FLAGS "-m elf_i386 -T src/boot/link.ld")
