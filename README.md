# lws-finnhub-client
A client that connects to Finnhub using the libwebsockets library, and dumps the incoming trades into a text file

## REQUIREMENTS
- libwebsockets library

## libwebsockets installation on Debian/Ubuntu

1. `git clone https://github.com/warmcat/libwebsockets.git`
2. cd to the libwebsockets directory
3. `sudo apt-get install libssl-dev`
4. `mkdir build`
5. `cd build`
6. `cmake ..`
7. `make`
8. `sudo make install`
9. `sudo ldconfig`

[Credits](https://stackoverflow.com/questions/29470447/how-can-i-install-the-libwebsocket-library-in-ubuntu)

## Usage

1. Enter your API key in line `220` 

![image](https://user-images.githubusercontent.com/45694080/171183033-f2e7b76d-4b90-4665-93c2-16ae161fec80.png)

2. `make`
3. `./client`

After a successful connection, the client will continue to run until the <kbd>Ctrl</kbd> + <kbd>Alt</kbd> signal is sent.

## Results
A .txt file will be created that contains all the incoming trades, as well as UNIX timestamp in milliseconds at the end of every received message from the server, depicting the time that the parsing of the message was done.
