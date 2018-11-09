# Fish Percolator stack for che

FROM eclipse/stack-base:debian

RUN echo "deb http://ftp.debian.org/debian buster main" > /etc/apt/sources.list.d/buster.list
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update -y && apt-get install -y chromium-driver nodejs ruby rubygems vim yarn && apt-get -t buster install -y postgresql-client-10 && apt-get clean

RUN gem install bundler
