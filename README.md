# corgi_ws

Clone this workspace in the $HOME directory.

### Install grpc
+ Official website: https://grpc.io/docs/languages/cpp/quickstart/

>>```
>>export MY_INSTALL_DIR=$HOME/corgi_ws/build
>>mkdir -p $MY_INSTALL_DIR
>>PATH="$MY_INSTALL_DIR/bin:$PATH"
>>cd ~/corgi_ws/build
>>git clone --recurse-submodules -b v1.62.0 --depth 1 --shallow-submodules https://github.com/grpc/grpc
>>cd grpc
>>mkdir -p cmake/build
>>pushd cmake/build
>>cmake -DgRPC_INSTALL=ON -DgRPC_BUILD_TESTS=OFF -DCMAKE_INSTALL_PREFIX=$HOME/corgi_ws/build ../..
>>make -j16
>>sudo make install
>>```

### Install other libraries
+ eigen: https://eigen.tuxfamily.org/index.php?title=Main_Page
+ mip_sdk: https://github.com/LORD-MicroStrain/mip_sdk.git
+ nlopt: https://github.com/stevengj/nlopt.git

>>```
>>cmake .. -DCMAKE_INSTALL_PREFIX=$HOME/corgi_ws/build
>>```

### Build corgi_core and corgi_system

Refers to the submodules

### Build corgi_sim

Refers to the submodules
