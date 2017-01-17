FROM centos:6.8

RUN yum install -y wget iputils git openssl-devel readline-devel zlib-devel gcc sqlite-devel gcc-c++ bzip2 mysql-server mysql mysql-devel
RUN git clone https://github.com/sstephenson/rbenv.git /root/.rbenv
RUN git clone https://github.com/sstephenson/ruby-build.git /root/.rbenv/ruby-build
RUN ./root/.rbenv/ruby-build/install.sh
ENV PATH /root/.rbenv/bin:$PATH
RUN echo 'eval "$(rbenv init -)"' >> /etc/profile
RUN echo 'eval "$(rbenv init -)"' >> .bashrc
RUN /root/.rbenv/bin/rbenv install 2.2.4
RUN /root/.rbenv/bin/rbenv global 2.2.4
RUN bash -l -c 'gem install bundler'
RUN bash -l -c 'gem install rails --no-ri --no-rdoc'
