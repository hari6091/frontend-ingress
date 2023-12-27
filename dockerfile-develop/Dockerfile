FROM nginx

WORKDIR /usr/share/nginx/html/

RUN apt-get update && apt-get install -y git

RUN rm -rf ./*

RUN git clone -b develop --single-branch https://github.com/hari6091/frontend-ingress.git .

EXPOSE 80

CMD ["/bin/bash", "-c", "git pull && nginx -g 'daemon off;'"]
