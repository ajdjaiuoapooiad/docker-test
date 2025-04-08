FROM ruby:3.2.2-alpine3.18

WORKDIR /var/www

COPY src/Gemfile src/Gemfile.lock ./
RUN gem update --system && \
    apk add --no-cache --update build-base ruby-dev && \
    bundle install

COPY src/. .

EXPOSE 4567
CMD ["rackup", "-p", "4567"]