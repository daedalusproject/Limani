ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y libcatalyst-perl \ 
 libcatalyst-plugin-configloader-perl \
 libcatalyst-plugin-static-simple-perl \
 libcatalyst-action-renderview-perl \
 libcatalyst-view-tt-perl libcatalyst-view-json-perl \
 libcatalyst-plugin-unicode-perl \
 libcatalyst-plugin-authentication-perl \
 libcatalyst-plugin-authorization-roles-perl \
 libnamespace-autoclean-perl \
 libmoose-perl libmoosex-nonmoose-perl \
 libconfig-general-perl \
 libcatalyst-model-adaptor-perl \
 libmoosex-markasmethods-perl \
 libcatalyst-modules-perl \
 libcatalyst-modules-extra-perl \
 libtext-csv-xs-perl \
 libcatalyst-model-adaptor-perl \
 libdbix-class-encodedcolumn-perl \
 libcatalyst-controller-formbuilder-perl \
 libconfig-zomg-perl \
 libterm-readkey-perl \
 libstring-random-perl \
 libdata-password-perl \
 libdbix-class-timestamp-perl \
 libcatalyst-authentication-store-dbix-class-perl \
 libcatalyst-action-rest-perl \
 libdata-password-check-perl \
 libdbix-class-validation-perl \
 libdatetime-format-sqlite-perl \
 libdaedalus-hermes-perl \
 libcatalyst-plugin-configloader-multi-perl \
 libcrypt-jwt-perl \
 libdatetime-format-mysql-perl \
 libnumber-phone-perl \
 libcatalyst-plugin-cache-perl \
 libredis-perl libcache-redis-perl \
 --no-install-recommends && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
