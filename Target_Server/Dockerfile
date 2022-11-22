FROM ubuntu:22.04

# Install OpenSSh server with apt
RUN apt update && apt install -y openssh-server openssh-client

# Created because public key is required when starting sshd
RUN ssh-keygen -A

# Create folders for sshd
RUN mkdir -p /run/sshd
RUN mkdir -p /var/run/sshd

# Specify root password
RUN echo 'root:root' | chpasswd

# Allow login as root
RUN sed -i 's/#\?PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config

# Expose port
EXPOSE 22

# Start sshd
CMD ["/usr/sbin/sshd", "-D"]