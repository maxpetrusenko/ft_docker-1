FROM ruby
RUN apt-get update -y && apt-get upgrade -y
RUN gem install rails
ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

#update and install rails
#docker build -t ex01 .
