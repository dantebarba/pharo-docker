#
# NOTE: THIS DOCKERFILE IS GENERATED VIA "update.sh"
#
# PLEASE DO NOT EDIT IT DIRECTLY.
#
FROM debian:jessie-slim

RUN set -ex \
	&& buildDeps='wget unzip' \
	&& runtimeDeps='ca-certificates libcairo2 libc6 libfreetype6 libssl1.0.0' \
	&& apt-get update \
	&& apt-get install -y --no-install-recommends $buildDeps $runtimeDeps \
	&& cd /usr/local/bin \
	&& wget -O- http://get.pharo.org/64/vm60 | bash \
	&& apt-get purge -y --auto-remove $buildDeps \
	&& rm -rf /var/lib/apt/lists/* \
	&& true 

CMD ["pharo"]
	
