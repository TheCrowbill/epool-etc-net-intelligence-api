EPool Ethereum Classic Network Intelligence API
============
[![Build Status][travis-image]][travis-url] [![dependency status][dep-image]][dep-url]


## Prerequisite
* partiy, classic geth
* node
* npm
* pm2

# Intall
git clone https://github.com/epoolio/epool-etc-net-intelligence-api/
cd epool-etc-et-intelligence-api
npm install pm2 -g
pm2 start app.json

## Configuration

Configure the app modifying [processes.json](/eth-net-intelligence-api/blob/master/processes.json). Note that you have to modify the backup processes.json file located in `./bin/processes.json` (to allow you to set your env vars without being rewritten when updating).

[
  {
    "name"              : "node-app",
    "script"            : "app.js",
    "log_date_format"   : "YYYY-MM-DD HH:mm Z",
    "merge_logs"        : false,
    "watch"             : false,
    "max_restarts"      : 10,
    "exec_interpreter"  : "node",
    "exec_mode"         : "fork_mode",
    "env":
    {
      "NODE_ENV"        : "production",
      "RPC_HOST"        : "localhost",
      "RPC_PORT"        : "8545",
      "LISTENING_PORT"  : "30303",
      "INSTANCE_NAME"   : "",
      "CONTACT_DETAILS" : "",
      "WS_SERVER"       : "wss://etcstats.epool.io",
      "WS_SECRET"       : "etcrocks",
      "VERBOSITY"       : 2
    }
  }
]




