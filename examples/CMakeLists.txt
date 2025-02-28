# Add your example source files and targets here
# For example:
# add_executable(my_example example_file.cpp)
# target_link_libraries(my_example ${LLVM_LIBRARIES})

add_executable(ConvolutionExample examples/ConvolutionExample.cpp)
target_link_libraries(ConvolutionExample PRIVATE ${LLVM_LIBRARIES} Optimization Kernels)
target_include_directories(ConvolutionExample PRIVATE ${LLVM_INCLUDE_DIRS})
llvm_map_components_to_libnames(LLVM_LIBRARIES Core ExecutionEngine Support)