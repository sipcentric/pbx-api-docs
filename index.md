### Introduction

The [Sipcentric PBX](http://www.sipcentric.com/) is a cloud-based service which enables businesses of all shapes and sizes to create a fully-featured, virtual PBX in minutes - allowing them to scale up or down instantly as their needs change and without commitment.

The Developer API, based around [REST](http://en.wikipedia.org/wiki/Representational_state_transfer) principles, allows users to interact with core features of the Sipcentric PBX platform and integrate with their own applications. The API makes it possible to programmatically manage features, query data and perform more interesting things such as initiating calls, sending text messages and hooking into specific real-time events and notifications (perfect for [screen popping](http://en.wikipedia.org/wiki/Screen_pop)).

### Current Version

The current stable version is v1 and is located at:

```
https://pbx.sipcentric.com/api/v1
```

Because the API follows many common REST design patterns, it is extremely easy to get started and is for the most part, self-documenting. Full documentation for this version, however, can be found [here](/api/v1).

### Example Uses

There are many ways in which developers can integrate their own applications with the Sipcentric PBX.

Some of our partners are using it to import their customer call records and other data into their own systems. We are also aware of some of our call centre customers using it to display real-time statistics on their wall displays, as well as integrating with in-house CRM systems. But the possibilities are virtually endless.

As a basic example of what can be achieved, we have developed the [Chrome Extension](http://www.sipcentric.com/internet-phone-service/google-chrome-extension/), available in the [Chrome Web Store](https://chrome.google.com/webstore/detail/sipcentric-for-chrome/kpiopepamhnnileoefikeakookcblmpc). The code is also available on [GitHub](https://github.com/sipcentric/chrome-extension).

### Getting Started

Before you can begin using the API, you'll need a Sipcentric PBX account. If you don't have one already, [create your account here](https://pbx.sipcentric.com/faces/signup/signup.xhtml) - it's free to get started and only takes a minute.

Once your account is activated, point your web browser at <a href="https://pbx.sipcentric.com/api/v1/customers/me" target="_blank">https://pbx.sipcentric.com/api/v1/customers/me</a> and log in using the credentials you supplied at sign-up.

You should see something like this:

```
{
  "type": "customer",
  "uri": "https://pbx.sipcentric.com/api/v1/customers/25",
  "created" : "2014-03-10T13:37:00.000+0000",
  "company": "Bloggs co",
  "firstName": "Fred",
  "lastName": "Bloggs",
  "telephone": "07557000000",
  "email": "contact@fredbloggs.com",
  "address1": "60 Cleveland St",
  "address2": "Fitzrovia",
  "city": "London",
  "postcode": "W1T 4JZ",
  "links": {
    "callBundles" : "https://pbx.sipcentric.com/api/v1/customers/25/callbundles",
    "recordings": "https://pbx.sipcentric.com/api/v1/customers/25/recordings",
    "phoneBook": "https://pbx.sipcentric.com/api/v1/customers/25/phonebook",
    "timeIntervals": "https://pbx.sipcentric.com/api/v1/customers/25/timeintervals",
    "endpoints": "https://pbx.sipcentric.com/api/v1/customers/25/endpoints",
    "phoneNumbers": "https://pbx.sipcentric.com/api/v1/customers/25/phonenumbers",
    "sms": "https://pbx.sipcentric.com/api/v1/customers/25/sms",
    "creditStatus": "https://pbx.sipcentric.com/api/v1/customers/25/creditstatus",
    "calls": "https://pbx.sipcentric.com/api/v1/customers/25/calls",
    "sounds": "https://pbx.sipcentric.com/api/v1/customers/25/sounds",
    "outgoingCallerIds": "https://pbx.sipcentric.com/api/v1/customers/25/outgoingcallerids"
  }
}
```

Congratulations - you have successfully made your first request to the Sipcentric API!

Ready to get creative? [Continue to full documentation...](/api/v1)

