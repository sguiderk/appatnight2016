# app@night2016

## Chatbots - the next big thing in technology


### Challenge A
Use the API of our career portal to create a new and innovative way of finding your potential dream job at Sixt.

#### API

##### Get all available jobs worldwide
```
GET https://api.sixt.jobs/jobs
```
Node example
```
const request = require('request');
request({
    uri: 'https://api.sixt.jobs/jobs',
    method: 'GET',
    gzip: true
  }, function (error, response, body) {
    if (!error && response.statusCode == 200) {
      var jobs = JSON.parse(body);
      // Your implementation
    } else {
      console.error("Failed calling JOBS API", response.statusCode, response.statusMessage, body.error);
    }
  });
```


##### Show job on career website

https://www2.sixt.jobs/de/en/jobs/3784

### Challenge B
Use our rental API to build a cutting-edge way, to find offers during a conversion with a bot.

#### API

##### Search for a SIXT station
```
GET https://app.sixt.de/php/mobilews/v4/stationsuggestion?address=München
GET https://app.sixt.de/php/mobilews/v4/stationsuggestion?latitude=48.1&longitude=11.5

Header:
Accept-Language: en_US
```

##### Get offers
```
GET https://app.sixt.de/php/mobilews/v4/offerlist?pickupStation=11&returnStation=11&pickupDate=2016-12-06T11:00:00+0100&returnDate=2016-12-09T11:00:00+0100

Header:
Accept-Language: en_US
```

##### Show offer on website

https://www.sixt.de/php/reservation/directoffer?ctyp=P&grp=CPMR&uci=11&rci=11&uda=20161205&rda=20161207&uti=1200&rti=1200&t=11

### Join the Slack Channel

https://appatnightslack.herokuapp.com

### Tools & Links
- https://ngrok.com Secure tunnels to localhost
- https://developer.facebook.com
- https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/getting-started-guide
- https://dev.kik.com/#/home
- https://github.com/howdyai/botkit/blob/master/readme.md#installation

