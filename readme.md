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

## Caveat

This will only delete your 3,200 most recent tweets. That's all that will get returned on your timeline, so if you're just trying to clear that it will work. If you want to delete more than 3,200 you'll need to download you data from twitter (which you can do in the account settings) and pull the older tweet id's out of the files.
