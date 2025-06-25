FROM nginx as web_container
LABEL "Project"="vprofile"
LABEL "Author"="TT"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/
