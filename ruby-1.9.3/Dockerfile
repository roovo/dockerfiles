FROM roovo/ruby-build:20140110.1

MAINTAINER roovo "roovo@roovoweb.com"

RUN \
  export RUBY_VERSION=1.9.3-p484 ;\
  echo "export RUBY_VERSION=$RUBY_VERSION" >> /.profile ;\
  echo "export PATH=/usr/local/lib/$RUBY_VERSION/bin:$PATH" >> /.profile ;\
  . /.profile ;\
  ruby-build -v $RUBY_VERSION /usr/local/lib/$RUBY_VERSION ;\
  echo "gem: --no-document" > /root/.gemrc ;\
  gem update --system 2.2.1 ;\
  gem install bundler ;\
# END RUN
