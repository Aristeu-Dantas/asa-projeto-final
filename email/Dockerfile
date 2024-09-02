FROM ubuntu:20.04

RUN apt update

RUN apt upgrade -y

RUN apt install postfix dovecot-imapd dovecot-pop3d -y

#COPY main.cf /etc/postfix
#
#COPY 10-auth.conf /etc/dovecot/conf.d

#Add User
RUN useradd -m aristeu

# Set user passord
RUN echo "aristeu:123"|chpasswd

#Add User
RUN useradd -m dantas

# Set user passord
RUN echo "dantas:123"|chpasswd

CMD ["/bin/bash", "-c", "service dovecot start; postfix start-fg"]
