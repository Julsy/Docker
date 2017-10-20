FROM            arhea/yarn:4
LABEL           maintainer="Iuliia Iliuk iiliuk@student.42.us.org"

WORKDIR         /usr/src/app

COPY            package.json /usr/src/app
COPY            yarn.lock /usr/src/app

RUN             yarn install

COPY            . /usr/src/app

EXPOSE          3000

CMD             [ "yarn" , "run" ]
