FROM ruby:2.5.1

RUN apt-get update -qq && apt-get install -y build-essential nodejs libpq-dev postgresql-client
RUN mkdir /app
WORKDIR /app
COPY Gemfile /app
COPY Gemfile.lock /app

RUN bundle install
COPY . /app
