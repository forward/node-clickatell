# node-clickatell

Client library for Clickatell SMS gateway.

## Installing

    npm install clickatell

## Example

    var click = require('clickatell');

    var sender = click.Clickatell({user: 'my@email.com', api_id: 1234, password: 'password'});
    sender.send('0700192919', 'Hello, World!', function(result) {
      console.log(result);
    });
    
