# Use the official image as a parent image.
FROM ruby:2.5.7

ENV BUNDLER_VERSION=2.1.4

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev\
    nodejs postgresql-client

RUN mkdir /app

WORKDIR /app

COPY ./Gemfile /app

RUN bundle install

COPY . /app

COPY entrypoint.sh /usr/bin/

RUN chmod +x /usr/bin/entrypoint.sh

ENTRYPOINT ["entrypoint.sh"]

EXPOSE 3000

# Start the main process.
CMD ["rails", "server", "-b", "0.0.0.0"]