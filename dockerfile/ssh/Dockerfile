FROM centos:centos7

MAINTAINER nick zhong_wei_cup@163.com

RUN yum install openssh-server -y

RUN /bin/echo "12345" | passwd --stdin root

RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key \
    && ssh-keygen -t rsa -f /etc/ssh/ssh_host_ecdsa_key \
    && ssh-keygen -t rsa -f /etc/ssh/ssh_host_ed25519_key

ADD run.sh /run.sh

RUN chmod 755 /run.sh

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]