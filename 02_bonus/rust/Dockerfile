FROM debian:jessie
LABEL maintainer="Iuliia Iliuk iiliuk@student.42.us.org"

# needed by cargo
ENV USER root

ADD install.sh install.sh
RUN chmod +x install.sh && ./install.sh && rm install.sh

VOLUME ["/source"]
WORKDIR /source
CMD ["bash"]
