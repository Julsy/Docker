FROM            ruby

LABEL           maintainer="Iuliia Iliuk iiliuk@student.42.us.org"

RUN             apt-get update -y && apt-get upgrade -y \
                && gem install rails \
                && apt-get install nodejs -y

ONBUILD COPY    . /opt/app
ONBUILD RUN     bundle install && db:migrate && rake db:seed --dir /opt/app
ONBUILD EXPOSE  3000
