
# Node js common error and quick solutions :

1. Node js build fail with error 


: request to http://repo.rammer.ai/repository/npm-dev/@rammerai-internal%2foauth2 failed, reason: connect ECONNREFUSED 35.223.153.54:80\n    at ClientRequest.req.on.err (/Users/vaishnavi/.nvm/versions/node/v8.17.0/lib/node_modules/npm/node_modules/node-fetch-npm/src/index.js:68:14)\n    at emitOne (events.js:116:13)\n    at ClientRequest.emit (events.js:211:7)\n    at Socket.socketErrorListener (_http_client.js:401:9)\n    at emitOne (events.js:116:13)\n    at Socket.emit (events.js:211:7)\n    at emitErrorNT (internal/streams/destroy.js:73:8)\n    at _combinedTickCallback (internal/process/next_tick.js:139:11)\n    at process._tickCallback (internal/process/next_tick.js:181:9)',


solution:
Open  .npmrc file verify repo path configured correctly or not should be below 
@rammerai-internal:registry=https://repo.rammer.ai/repository/npm-dev/
@rammerai:registry=https://repo.rammer.ai/repository/public/

