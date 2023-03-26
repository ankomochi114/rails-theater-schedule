FROM ruby:3.2.1

ENV LANG=C.UTF-8 \
  TZ=Asia/Tokyo

RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    default-mysql-client \
    nodejs \
    sudo \
    vim

RUN mkdir /api
WORKDIR /api
COPY Gemfile /api/
COPY Gemfile.lock /api/
RUN bundle install

CMD ["rails", "server", "-b", "0.0.0.0"]
