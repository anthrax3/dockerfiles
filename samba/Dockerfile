FROM		debian:latest
# CMDBUILD	docker build -t svendowideit/samba https://raw.githubusercontent.com/SvenDowideit/dockerfiles/master/samba/Dockerfile
# CMDRUN		docker run svendowideit/samba

MAINTAINER	Sven Dowideit <SvenDowideit@docker.com> (@SvenDowideit)

# gettext for envsubst
RUN		apt-get update && \
               apt-get install -yq samba gettext && \
               rm -rf /var/lib/apt/lists/*

ADD		share.tmpl setup.sh /

ENTRYPOINT      ["/setup.sh"]
