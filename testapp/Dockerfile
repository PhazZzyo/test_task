FROM ruby:2.5

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /testapp
WORKDIR /testapp
COPY Gemfile /testapp/Gemfile
COPY Gemfile.lock /testapp/Gemfile.lock
RUN bundle install
COPY . /testapp
CMD ["config/puma.rb"]
