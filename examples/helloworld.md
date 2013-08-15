# Hello World

### Making your first call using the Sipcentric API.

To dial a number from a phone extension you need to send a HTTP POST request to `http://pbx.sipcentric.com/api/v1/customers/me/calls` with a JSON body containing the required call infomation:

	{
		"type": "call",
		"endpoint": "http://pbx.sipcentric.com/api/v1/customers/me/endpoints/1234",
		"to": "12345"
	}

The "endpoint" is the phone extension you want the call to originate from. The endpoint ID is a unique URL which you can find from: `http://pbx.sipcentric.com/api/v1/customers/me/endpoints`

Then the "to" is obviously the number you want the call made to. This can be any number you would be able to dial from a extension.

## Linux

Here is an example cURL request for initiating a call:

	curl --user username:password -v -X POST -H "Content-Type: application/json" -d '{"type":"call","endpoint":"http://pbx.sipcentric.com/api/v1/customers/me/endpoints/12345","to":"07123456"}' http://pbx.sipcentric.com/api/v1/customers/me/calls

## Node.js

	var username = '';
	var password = '';

	function call(number) {
		var request = require('request');

		var options = {
			uri: 'http://pbx.sipcentric.com/api/v1/customers/me/calls',
			method: 'POST',
			headers: { 'Authorization': 'Basic ' + new Buffer(username + ':' + password).toString('base64') },
			json: {
				"type":"call", "endpoint":"http://pbx.sipcentric.com/api/v1/customers/me/endpoints/001122", "to":number
			}
		};

		request(options, function (error, response, body) {
			if (!error && response.statusCode == 200) {
				console.log("Request Successful!");
			} else {
				console.log("Something went wrong: " + response);
			}
		});
	}

	call("0123456789");

When the request is made you should get a 200 OK response back and the endpoint extension will start to ring.