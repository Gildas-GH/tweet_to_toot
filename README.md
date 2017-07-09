# tweet\_to\_toot

A tool for tooting tweets from your favorite accounts
This repo is a fork of [this repository](https://github.com/jstumbaugh/tweet_to_toot) with some changes :
- I deleted "@twitter-username: " at the beginning of the toot
- The script now check new tweets every 30 seconds instead of 1 hour

You will need [Ruby 2.2.4](https://tecadmin.net/install-ruby-on-rails-on-ubuntu/)
rails (```gem install rails```),
bundle (```gem install bundle```),
Docker (add ```deb http://httpredir.debian.org/debian jessie-backports main``` to /etc/apt/sources.list, run ```apt-get update``` and then ```apt-get install docker.io```).

## Steps to install

### 1. Clone the Repository

```
git clone https://github.com/jstumbaugh/tweet-to-toot
```

### 2. Create a Twitter app to get the access keys

Create a [twitter app](https://apps.twitter.com/app/new) and generate access
tokens. Store these in the `env_example` file.

### 3. Create a Mastodon Account to post the Tweets to

Store the instance URL, login email, and password in the `env_example` file.

### 4. Pick the Twitter Accounts to follow and post to Mastodon

Store these account handles in the `env_example` file.

```env
# Twitter handles in a comma separated list
TWITTER_HANDLES_TO_TOOT='RubyInside, rubyflow'
```

Now, rename ```env_exemple``` to ```.env```.

### 5. Run the task to toot tweets

You can run the rake task

```
bundle exec rake
```

## Enjoy!
