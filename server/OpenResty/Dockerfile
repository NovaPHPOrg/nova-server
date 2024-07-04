# Dockerfile - alpine-fat
# https://github.com/openresty/docker-openresty
#
# This builds upon the base OpenResty alpine image that adds
# some build-related packages, has perl installed for opm,
# and includes luarocks and envsubst.

ARG RESTY_IMAGE_BASE="openresty/openresty"
ARG RESTY_IMAGE_TAG="alpine"

FROM ${RESTY_IMAGE_BASE}:${RESTY_IMAGE_TAG}

RUN apk add perl \
curl \
 &&  opm get Kiuber/lua-resty-waf

USER root 

COPY nginx.conf /usr/local/openresty/nginx/conf/nginx.conf