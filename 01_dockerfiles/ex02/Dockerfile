FROM ruby:2.6.4
RUN apt update
RUN apt install -y nodejs gem git
RUN gem install rails -v 5.2.3
RUN gem install bundler
RUN git clone https://github.com/alaghlid/my_rubby_app.git  /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate

# docker build -f Dockerfile -t ft-rails:on-build .
# docker build -f Dockerfile2 -t test .
# docker run -it -p 3000:3000 -d test
