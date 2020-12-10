# Use the official image as a parent image.
FROM ruby:2.5.7

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev\
    nodejs postgresql-client

WORKDIR /api

COPY Gemfile /api/Gemfile

COPY Gemfile.lock /api/Gemfile.lock

RUN gem install bundler

RUN bundle install

COPY . /api

COPY entrypoint.sh /usr/bin/

RUN chmod +x /usr/bin/entrypoint.sh

ENTRYPOINT ["entrypoint.sh"]

EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]