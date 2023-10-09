FROM nginx

ARG UNAME=user
ARG UID=1001
ARG GUID=1001

COPY default.conf /etc/nginx/conf.d/
RUN mkdir /app
COPY homework.html /app

RUN groupadd -g $GUID -o $UNAME && useradd -m -u $UID -g 1001 -o -s /bin/bash $UNAME
RUN chown -R user:nginx /usr/share/nginx/html

EXPOSE 8000



