# Thinking about this project, its progress and its goals.

* [chimes](../chime/index.md)

I find that wrinting down my thinking helps me staying focused, constratined and finding ways formward to solutions and answers.

## 20260822

I had an error in the built Github Pages. The generated site had links that went to my Cratchit-repo/site?

* It turned out the the _config.yml file I had copied contained urls!
* So I tried to make a super clean _config.yml with no repo-specific meta-data at all.
* So far it seems to work just fine?

  * The generated site still looks fine?
  * And now the links are all as I expect within this repo.

* Although I am still a little unsure if the site I see is the latest built one?

  * I did refresh in macOS Safari and the previous errors disappeared.
  * But that was for a site built form a fixed _config.yml (still URLs but correct ones)

* I triggered a rebuild of Github pages but still seem to take forever?
* Maybe Githup prioritise build triggered by commits to the repo?

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
