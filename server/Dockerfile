FROM ruby:2.5.1
RUN apt-get update -qq && apt-get install -y  build-essential libpq-dev nodejs
RUN mkdir /usr/src/turfs
WORKDIR /usr/src/turfs
ADD Gemfile      /usr/src/turfs/Gemfile
ADD Gemfile.lock /usr/src/turfs/Gemfile.lock
RUN bundle install
ADD . /usr/src/turfs
