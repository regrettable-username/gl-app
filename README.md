# GL App Template

This is a template for a simple imgui based SDL/OpenGL3 application. It is intended to be used as a starting point for new projects. It supports native and wasm builds.

Note: This is just taking out the imgui example for SDL2/GL3 and putting it into a reusable repo for future projects.

## Building

## MacOS and Linux Native
1. You need to install SDL 2 via your package manager or build it from source. See [here](https://wiki.libsdl.org/SDL2/Installation) for more information.
2. Now clone this repo and build:
  ```bash
    git clone git@github.com:regrettable-username/gl-app.git --recursive
    cd gl-app/build
    make -j4
    ./gl-app
  ```
  You should see the imgui demo pop up.

  ## WASM
  1. You first need to set up emsdk. Follow the instructions [here](https://emscripten.org/docs/getting_started/downloads.html). Be sure to source the emsdk_env.sh script so the emsdk environment variables are set!
2. Now clone this repo and build:
  ```bash
    git clone git@github.com:regrettable-username/gl-app.git --recursive
    cd gl-app/build-wasm
    make -f Makefile.emscripten -j4 serve
  ```
  Note: You may get a prompt to allow incoming connections when you run the server. You'll need to allow this for the server to accept connections on your local machine. This is the case at least on macOS.
  3. Open your browser to localhost:8000 and you should see the imgui demo pop up.
