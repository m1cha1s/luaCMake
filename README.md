# Lua
This is a fork of the lua programming language that is converted to CMake. It presents it self with two targets: luaLub and lua. The lua target is used to build lua programming language. LuaLib is a target used to embed lua in your C/C++ project.

## Example of use as library
### yourProjectDir:
- src/
- build/
- CMakeLists.txt
- luaCMake (git submodule for example)
### In your CMakeLists.txt add:
```
add_subdirectory(luaCMake)
target_link_libraries(<your target> PRIVATE luaLib)
```