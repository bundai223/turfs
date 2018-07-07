FROM ruby:2.5.1

ENV APP_ROOT /turfs

WORKDIR $APP_ROOT

RUN apt-get update -qq && apt-get install -y  build-essential libpq-dev nodejs

ADD Gemfile $APP_ROOT/Gemfile
ADD Gemfile.lock $APP_ROOT/Gemfile

RUN bundle install

ADD . $APP_ROOT
