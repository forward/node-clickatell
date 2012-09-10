# node-clickatell

Client library for Clickatell SMS gateway.

## Installing

    npm install clickatell

## Example

### With Default Sender ID
    var click = require('clickatell');

    var sender = click.Clickatell({user: 'my@email.com', api_id: 1234, password: 'password'});
    sender.send('0700192919', 'Hello, World!', function(result) {
      console.log(result);
    });
    
### With Authorized Sender ID
After adding your sender ID and it gets approved [Clickatell Central > Manage Sender IDs](https://central.clickatell.com/central/central/dashboard/senderid_dashboard.php), use the from option like this:

    var click = require('clickatell');

    var sender = click.Clickatell({user: 'my@email.com', api_id: 1234, password: 'password', from: 'SENDER_ID'});
    sender.send('0700192919', 'Hello, World!', function(result) {
      console.log(result);
    });
    