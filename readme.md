# Tweet-delete

A lambda which will delete tweets older than a defined time period from twitter.

## Installation

This assumes you've already [set up your AWS account to work with serverless](https://www.serverless.com/framework/docs/providers/aws/guide/credentials/).

Make a copy of `config.example.yml` and name it `config.yml`.

Create [a new twitter app](https://developer.twitter.com/en/apps) and paste the relevant keys and secrets into your new `config.yml`.


In your terminal run:

```bash
$ npm install
$ npm run deploy
```

The lambda will now run once a day and delete any new tweets which are older than the allowed time. The first run through will obviously take longer as it clears out old tweets.
