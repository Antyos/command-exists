command-exists
==============

node module to check if a command-line command exists



## installation

npm install command-exists

## usage

### async

```js
var commandExists = require('command-exists');

commandExists('ls', function(err, commandExists) {

    if(commandExists) {
        // proceed confidently knowing this command is available
    }

});
```
### promise
```js
var commandExists = require('command-exists');

// invoked without a callback, it returns a promise
commandExists('ls')
.then(function(command){
    // proceed
}).catch(function(){
    // command doesn't exist
});
```

### sync
```js
var commandExistsSync = require('command-exists').sync;
// returns true/false; doesn't throw
if (commandExistsSync('ls')) {
    // proceed
} else {
    // ...
}

```
