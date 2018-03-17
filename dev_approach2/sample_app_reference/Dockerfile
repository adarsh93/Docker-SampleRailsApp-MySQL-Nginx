# Rails Sample App
# Version 1.1

FROM ruby:latest

# Include the library for mysqlclient
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs default-libmysqlclient-dev
RUN mkdir /sampleapp
WORKDIR /sampleapp

# Copy the Gemfile to container and run bundle to install required dependencies
COPY Gemfile /sampleapp/Gemfile
COPY Gemfile.lock /sampleapp/Gemfile.lock
RUN bundle install
