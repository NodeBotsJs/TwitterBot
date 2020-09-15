# TwitterBot
A simple bot in Twit for Twitter

# How to setup
How to set the bot?

Create a file named: `.env`

Inside it you put: 
```
CONSUMER_KEY=consumerkey
CONSUMER_SECRET=consumersecret
ACCESS_TOKEN=accesstoken
ACCESS_TOKEN_SECRET=accesstokensecret
```

# How does my bot start?
`index.js`

```const Twit = require('twit');
const T = new Twit({
  consumer_key: process.env.CONSUMER_KEY,
  consumer_secret: process.env.CONSUMER_SECRET,
  access_token: process.env.ACCESS_TOKEN,
  access_token_secret: process.env.ACCESS_TOKEN_SECRET
});
// start stream and track tweets
const stream = T.stream('statuses/filter', {track: '#JavaScript'});
// event handler
stream.on('tweet', tweet => {
// perform some action here
});```

# At the terminal
#1
```
$ npm init
```

#2
```
$ npm i twit
```

#3
```
$ node .
```


To find out how to create your bot account see [this link](https://blog.devmountain.com/its-alive-how-to-make-a-twitter-bot-in-five-steps/)
