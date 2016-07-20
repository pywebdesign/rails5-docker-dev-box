FROM ruby:2.3
RUN mkdir /app
RUN mkdir /app/vendor
RUN mkdir /app/vendor/bundle
WORKDIR /app
ADD ./bundle.config /root/.bundle/config
env BUNDLE_PATH vendor/bundle

RUN apt-get update -y && apt-get install -y nodejs && apt-get install -y npm
RUN npm cache clean -f && npm install -g n && n stable