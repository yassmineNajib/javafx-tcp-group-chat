# JavaFX TCP Group Chat

A desktop group-chat application built in Java 17 with JavaFX, TCP sockets, multithreading, and a model/view separation of concerns.

## Features

- A JavaFX server dashboard that starts and monitors the chat server.
- Multiple TCP clients that join the same group chat.
- Timestamped messages with join and leave notifications.
- A connected-user list requested through the `allUsers` command.
- Read-only guest mode when a client connects without a username.
- Graceful disconnect through `end` or `bye`.
- Configurable server host and port in `server/src/main/resources/config.properties`.

## Project structure

```text
server/  JavaFX TCP server and connection-handling logic
client/  JavaFX TCP client and chat interface
```

## Requirements

- JDK 17 or newer
- Maven 3.9 or newer

## Build

From the project root:

```bash
mvn clean package
```

## Run

Start the server first:

```bash
mvn -pl server exec:java
```

Then start one or more clients in separate terminals:

```bash
mvn -pl client exec:java
```

The default configuration listens on port `3000`. For a client on another computer, use the server machine's reachable IP address and allow that port through the firewall.

## Notes

Generated Maven output, IDE settings, macOS ZIP metadata, and compiled JavaFX libraries are intentionally excluded from Git. Maven recreates them when the project is built.
