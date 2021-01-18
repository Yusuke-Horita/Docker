FROM ruby:2.5.7

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs default-mysql-client vim

RUN mkdir /aaa

WORKDIR /aaa

COPY Gemfile /aaa/Gemfile
COPY Gemfile.lock /aaa/Gemfile.lock

RUN gem install bundler
RUN bundle install

COPY . /aaa