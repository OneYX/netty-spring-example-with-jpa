# TCP-Communication-Service
TCP communication server with Netty, spring-boot, spring-data-jpa

This TCP Communication Service is a simple example for developer who want to make tcp service with Spring-Boot, Spring-Data-JPA and Netty.


## Feature
* Telnet Client can send message to other telnet client.
* Telnet Client can retrieve User Information from RDBMS(H2 DB).

## How to use
* Run com.zbum.example.socket.server.netty.Application with IDE or Maven
```
    $ mvn spring-boot:run
```
* Connect to this server by telnet command.
```
    $ telnet localhost 8090
    Trying ::1...
    Connected to localhost.
    Escape character is '^]'.
    Your channel key is /0:0:0:0:0:0:0:1:57220
```
* Your channel key (ID) is 04e9b346-50ec-4810-bd59-6daba2cc6f54
* Connect to this server by telnet command on annother terminal.
```
    $ telnet localhost 8090
    Trying ::1...
    Connected to localhost.
    Escape character is '^]'.
    Your channel key is /0:0:0:0:0:0:0:1:57221
```
* From now, you can send message to 04e9b346-50ec-4810-bd59-6daba2cc6f54 channel by below
```
    /0:0:0:0:0:0:0:1:57220::I Love You!!!
```
* Then, you can receive Message like below
```bash
    $ telnet localhost 8090
    Trying ::1...
    Connected to localhost.
    Escape character is '^]'.
    Your channel key is /0:0:0:0:0:0:0:1:57220
    I Love You!!!
```


