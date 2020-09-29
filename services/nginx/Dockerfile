FROM docker.miracum.org/cbioportal/cbioportal:${RELEASE:-latest} as static

FROM nginx:stable-alpine
COPY --from=static /cbioportal-webapp /usr/share/nginx/html
RUN rm /etc/nginx/conf.d/default.conf
COPY ./genomenexus.conf /etc/nginx/conf.d/default.conf
