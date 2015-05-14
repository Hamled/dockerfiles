# From: https://github.com/codenvy/dockerfiles/blob/master/base/ruby210/Dockerfile

FROM codenvy/shellinabox

ENV DEBIAN_FRONTEND noninteractive
ENV RUBY_VERSION 2.2.2
RUN sudo apt-get update && \
    sudo -E apt-get install -y nodejs curl && \
    curl -sSL https://rvm.io/mpapis.asc | sudo gpg --import - && \
    curl -sSL https://get.rvm.io | sudo bash -s stable && \
    sudo /bin/bash -l -c "rvm requirements" && \
    sudo /bin/bash -l -c "rvm install ${RUBY_VERSION}"

RUN sudo sed -i '/exec "$@"/isource /etc/profile.d/rvm.sh\n' /entrypoint.sh
