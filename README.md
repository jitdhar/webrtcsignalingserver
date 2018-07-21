

## Running

Running the server requires a valid installation of node.js which can be installed from the nodejs.org website. After installing the package you will need to install the node dependencies.

1) npm install

2) run the server using "node server.js"

3) In the console you will see a message which tells you where the server is running:

                        "signal master is running at: http://localhost:8888"

4) Open a web browser to the specified URL and port to ensure that the server is running properly. You should see the message when you go to the /socket.io/ subfolder (e.g. http://localhost:8888/socket.io/), you should see a message like this:

						{"code":0,"message":"Transport unknown"}

### Production Environment
* generate your ssl certs

```shell
$ ./scripts/generate-ssl-certs.sh
```
* run in Production mode

```shell
$ NODE_ENV=production node server.js
```

## Use with Express
    var express = require('express')
    var sockets = require('signalmaster/sockets')

    var app = express()
    var server = app.listen(port)
    sockets(server, config) // config is the same that server.js uses


