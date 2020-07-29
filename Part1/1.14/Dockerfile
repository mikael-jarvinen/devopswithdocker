FROM ruby:2.6.0

RUN apt-get update && apt-get install -y git curl
RUN gem install bundler
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get update && apt-get install -y nodejs

RUN git clone https://github.com/docker-hy/rails-example-project.git server
WORKDIR server/

RUN bundle install
RUN rails db:migrate

EXPOSE 3000
CMD ["rails", "s"]
