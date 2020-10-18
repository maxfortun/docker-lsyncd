FROM alpine:edge

RUN echo https://dl-cdn.alpinelinux.org/alpine/edge/testing >> /etc/apk/repositories

RUN apk --update add openssh-client rsync lsyncd && \
	echo 'StrictHostKeyChecking=no' >> /etc/ssh/ssh_config && \
	mkdir /root/.ssh && \
	chmod -R og-rwx /root/.ssh 

CMD [ "lsyncd", "-nodaemon", "-delay", "0", "/etc/lsyncd.conf" ]

