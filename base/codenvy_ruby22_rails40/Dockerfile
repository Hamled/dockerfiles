# From: https://github.com/codenvy/dockerfiles/blob/master/base/ruby210_rails403/Dockerfile

FROM hamled/codenvy_ruby22

RUN sudo /bin/bash -l -c "gem install bundler --no-ri --no-rdoc"
EXPOSE 3000
ENV CODENVY_APP_PORT_3000_HTTP 3000
