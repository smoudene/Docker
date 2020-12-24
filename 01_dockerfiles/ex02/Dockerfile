FROM ruby:2.6.5
RUN apt-get update -y && apt-get install -y build-essential libpq-dev nodejs sqlite3

RUN gem update && gem install rails -v 5.2.3
RUN	gem install rake -v 13.0.1
RUN gem install bundler
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake _13.0.1_ db:migrate
ONBUILD RUN rake _13.0.1_ db:seed
