cmake_minimum_required (VERSION 3.18)

project(CudaBmk)

set(CMAKE_CUDA_ARCHITECTURES 52 61 70 75)
enable_language(CUDA)

add_executable(cmem cmem.cu)
add_executable(diverge diverge.cu diverge2.cu diverge3.cu path.cu)
add_executable(global global.cu)
add_executable(icache icache.cu icache_kernels1.cu icache_kernels2.cu icache_kernels3.cu icache_kernels4.cu)
add_executable(shared shared.cu)
add_executable(sync sync.cu sync2.cu)
add_executable(texture2 texture2.cu)
add_executable(texture4 texture4.cu)
