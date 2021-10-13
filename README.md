
https://pspdfkit.com/blog/2020/visual-studio-code-cpp-docker/

CMake will configure and generate makefiles by default, set all options to their default settings and cache them into a file called CMakeCache.txt in the build directory.
cmake -S . -B build

invoke your build system
cmake --build build

run your tests
cmake --build build --target test

Debugging your CMake files
--trace option will print every line of CMake that is run
--trace-source="filename", which will print out every executed line of just the file you are interested in

cmake build --trace-source="CMakeLists.txt"