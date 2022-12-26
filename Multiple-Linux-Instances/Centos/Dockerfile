FROM centos:7
RUN yum install openssh-server openssh-clients vim mlocate curl wget net-tools ansible sudo -y
RUN yum install epel-release -y
RUN  yum install ansible -y
RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config
RUN ssh-keygen -A
RUN echo "root:centos" | chpasswd
RUN useradd -rm -d /home/mahsan -s /bin/bash -g root -u 1001 mahsan -p "$(openssl passwd -1 redhat64 )"
RUN echo "mahsan  ALL=(ALL)  NOPASSWD: ALL" >> /etc/sudoers
CMD ["/usr/sbin/sshd", "-D"]

