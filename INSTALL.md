## Install

### With submodules
1. Use `git clone https://github.com/filrin123/socket.io-client-cpp.git` to clone your local repo.
2. Run `cd socket.io-client-cpp`
3. Run `git submodule update --init --recursive` to download submodules.
4. Run `cmake -DUSE_SUBMODULES=ON -DCMAKE_EXPORT_COMPILE_COMMANDS=1 .` to generate `Makefile` and `compile_commands.json`.
5. Run `make` to build the project.
6. Run `sudo make install` to install the library to your system.

### Without submodules
1. Use `git clone https://github.com/filrin123/socket.io-client-cpp.git` to clone your local repo.
2. Run `git clone https://github.com/zaphoyd/websocketpp.git` to download websocketpp library.
3. Run `sudo cp -r websocketpp/websocketpp /usr/local/include/` to install websocketpp library.
4. Run `sudo apt-get install cmake openssl libssl-dev libboost-all-dev libasio-dev rapidjson-dev` to install all other libraries and dependencies.
5. Run `cd socket.io-client-cpp`
6. Run `cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=1 .` to generate `Makefile` and `compile_commands.json`.
7. Run `make` to build the project.
8. Run `sudo make install` to install the library to your system.

## Uninstall
1. Run `cd /usr/local/include && sudo rm sio_client.h sio_message.h sio_socket.h`
2. Run `cd /usr/local/lib && sudo rm libsioclient.a libsioclient_tls.a`
3. Run `sudo rm /usr/local/lib/cmake/sioclient`

(Basically remove all the files that `sudo make install` told it installed)

Tested only on Ubuntu Desktop 23.10.