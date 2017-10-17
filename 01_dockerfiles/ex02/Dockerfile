# to check:
# in ex02 run "docker build -t ft-rails . "
# then cd ../hello_app
# run "docker build -t new_rails_app . "
# and "docker run -d -p 3000:3000 new_rails_app"

FROM            ruby

LABEL           maintainer="Iuliia Iliuk iiliuk@student.42.us.org"

RUN             apt-get update -y && apt-get upgrade -y \
                && apt-get install -y nodejs \
                && gem install rails \
                && mkdir -p /opt/app

ONBUILD COPY    . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD EXPOSE  3000
ONBUILD RUN     bundle install && rake db:migrate && rake db:seed
