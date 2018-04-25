FROM nginx:1.13.12

# Change Timezone
ARG TIME_ZONE=UTC
ENV TIME_ZONE ${TIME_ZONE}
RUN ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo $TIME_ZONE > /etc/timezone

# Change Webroot Permissions
RUN mkdir /var/www
RUN chown -R www.www /var/www/ /var/log/nginx/
