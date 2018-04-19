FROM ruby:2.3.1-alpine
RUN apk add --update tzdata curl
WORKDIR /usr/local/src
ONBUILD COPY --from=builder /usr/local/bundle /usr/local/bundle
ONBUILD COPY . /usr/local/src
ONBUILD RUN bundle install --local
