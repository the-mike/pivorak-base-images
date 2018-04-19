FROM ruby:2.3.1-alpine

RUN apk --update add \
    build-base linux-headers \
    mysql-dev qt qt-dev git \
    mariadb-client mariadb-client-libs tzdata pcre libstdc++ \
    gcc g++ make curl-dev pcre-dev wget nodejs xvfb socat postgresql-dev

WORKDIR /usr/local/src
RUN gem install bundler
ONBUILD COPY Gemfile* *.gemspec ./
# ONBUILD RUN bundle install --without local
