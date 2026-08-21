# Thinking about this project, its progress and its goals.

I find that wrinting down my thinking helps me staying focused, constratined and finding ways formward to solutions and answers.

## 20260821

So I actually used coPilot to inject content to the scaffolding I created ,manually.

* I created the repo as a Github repo and cloded it.

  * I chose Apache GNU GENERAL PUBLIC LICENSE Version 2, June 1991 (same as Linux)
  * I created README.md
  * I created docs/thining.md
  * I added documentation support 'init_new.py' and 'update_index.py'
  * added ampty CMakeLists.txt and src/main.cpp

* I then prompted coPilot to fill in the scaffolding for a cross platform C++ concole CLI app.

  * It injected content into CMakeLists.txt

  ```sh
  cmake_minimum_required(VERSION 3.20)

  project(cpp_habilis VERSION 0.1.0 LANGUAGES CXX)

  add_executable(cpp_habilis
    src/main.cpp
  )

  target_compile_features(cpp_habilis PRIVATE cxx_std_20)

  if(MSVC)
    target_compile_options(cpp_habilis PRIVATE /W4 /permissive-)
  else()
    target_compile_options(cpp_habilis PRIVATE -Wall -Wextra -Wpedantic)
  endif()

  include(GNUInstallDirs)
  install(TARGETS cpp_habilis
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
  )
  ```

  * I interrogated coPiot about cmake semantics and edited the CMakeLists.txt

  ```sh
  
  ```
