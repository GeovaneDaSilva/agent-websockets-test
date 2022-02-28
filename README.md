# agent-test

## Project setup
```
npm install
```

### Run Live Server
```
npm run serve
```

### Visit

http://localhost:8080/

### How to use it

Set a valid url, signed with the same value as the environment variable 'SOCKET_PROXY_SECRET'

example:

ws://localhost:5000/signed/listen/eyJfcmFpbHMiOnsibWVzc2FnZSI6ImV5SnNhV05sYm5ObFgydGxlU0k2SWpJeU16UTJPVGsxWmkwek1TSjkiLCJleHAiOiIyMDIxLTA3LTIyVDEwOjA2OjUzLjgyNFoiLCJwdXIiOm51bGx9fQ==--77e05da89f523401d874ad5b7923230a0f067ed91df22bdee6e1adee73e155ff/EBB3A27D170B2A74A8D13942A5496

ws://<socket_host>:<socket_port>/signed/listen/<signed-token>/<device_id>

### Send events to the socket

When connecting to the server, it should respond with two messages that will be reflected on the screen
["ready", "connected"] if there is any error they will be reflected on the screen

Select what type of message you want to send, when receiving it the socket will show in the console all the messages that are being added to the redis queue, in the instance 'process.env.REDIS_URL'.
