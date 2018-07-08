FROM ruby:2.5.1
RUN apt-get update -qq && apt-get install -y  build-essential libpq-dev
# yarnパッケージ管理ツールインストール
RUN apt-get update && apt-get install -y curl apt-transport-https wget && \
  curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
  apt-get update && apt-get install -y yarn
# Node.jsをインストール
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && apt-get install nodejs

RUN mkdir /usr/src/turfs
WORKDIR /usr/src/turfs
ADD Gemfile      /usr/src/turfs/Gemfile
ADD Gemfile.lock /usr/src/turfs/Gemfile.lock
RUN bundle install
ADD . /usr/src/turfs
