# Prompting node #

    node app.js

This will run your script `app.js` akin to python `app.py`

    node --version

 will get you, your current version

# Window vs global #

Usually prefixed with window e.g. `window.console.log();`
with node we don't window, so instead we have global e.g. `global.console.log();`
but we don't need to reference global explicitly.

    console.log(); # Log to console
    setTimeout(); # Call a function after a delay

## Importing modules ##

use require and we want to use const for importing modules.

`import panas as pd`

in js if there were pandas it would be

`const pd = require('pandas')`

### We want to import logger.js ###

    // code for logger js
    var hugs = 5;

    function prnt(msg) {
        return msg;
    }

    module.exports.hugs = hugs;
    module.exports.printer = prnt;

Same dir with a file called app.js

    // code for app.js
    const logger = require('./logger');

    console.log(logger.printer('hello'));


# Useful Modules #

### Pathing ###

Interacting with pathing/directories

    const path = require('path')
    
    var pathObj = path.parse(__filename)
    var fileNameObj = path.parse(__dirname)

### OS ###

Interact with the operating system

    const os = require('os)

    var totalMemory = os.totalmem();

### File System ###

Interacting with files/file system

    const fs = require('fs)

    const files = fs.readdirSync('./) // show all files in pwd

    console.log('files)


# Resources #

- https://nodejs.org/docs/latest-v0.10.x/api/
- https://www.youtube.com/watch?v=TlB_eWDSMt4
