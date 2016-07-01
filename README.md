# applepayjs
Apple Pay JS integration with Stripe

The stable release will be available this fall probably.

First thing you want to do if you are able to do the Apple Pay requests:

    ApplePaySession.canMakePayments()

Then the transaction itself:

    var request = {
      countryCode: 'US',
      currencyCode: 'USD',
      supportedNetworks: ['visa', 'masterCard'],
      merchantCapabilities: ['supports3DS'],
      total: { label: 'Your Label', amount: '10.00' },
    }
    var session = new ApplePaySession(1, request);

This is from official website how to get it started: https://developer.apple.com/reference/applepayjs/applepaysession

After you have the session, you can control it:
[![enter image description here][1]][1]


And you can listen to events, and change your flow based on it:
[![enter image description here][2]][2]


  [1]: http://i.stack.imgur.com/ONPbv.png
  [2]: http://i.stack.imgur.com/SHckj.png
