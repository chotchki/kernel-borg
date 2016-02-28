cmake_minimum_required (VERSION 2.6)
project (Kernel-Borg C ASM)

set_source_files_properties(src/boot/boot.asm PROPERTIES COMPILE_FLAGS "-x assembler-with-cpp")
add_executable(kernel src/boot/boot.asm src/kmain.cpp)
