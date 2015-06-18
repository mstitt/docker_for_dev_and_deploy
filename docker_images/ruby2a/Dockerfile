
FROM local/ziggy_user
USER root

RUN apt-get update && apt-get install --yes zlib1g-dev libssl-dev libreadline6-dev libyaml-dev libncurses5-dev libffi-dev libgdbm3 libgdbm-dev

RUN wget http://cache.ruby-lang.org/pub/ruby/2.1/ruby-2.1.2.tar.gz -O- | tar zxf -
RUN cd ruby-2.1.2 && ./configure --disable-install-doc && make && make install && cd .. && rm -rf ruby-2.1.2 && rm -f ruby-2.1.2.tar.gz
RUN gem install bundler --no-rdoc --no-ri

USER ziggy
