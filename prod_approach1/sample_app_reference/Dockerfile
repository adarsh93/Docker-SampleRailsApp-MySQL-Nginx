# Rails Sample App
# Version 1.0

FROM ruby:latest

# Include the library for mysqlclient
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs default-libmysqlclient-dev

# Create a directory in the container for the application
RUN mkdir /sampleapp
WORKDIR /sampleapp

# Copy the Gemfile to the container and run bundle to install all required dependencies
COPY Gemfile /sampleapp/Gemfile
COPY Gemfile.lock /sampleapp/Gemfile.lock
RUN bundle install

# Copy the application code to the container
COPY . /sampleapp
