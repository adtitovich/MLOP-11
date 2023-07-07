# Use the official image as a parent image
FROM ubuntu
 
# Update the system
RUN apt update && apt upgrade -y
 
# Install OpenSSH Server
RUN apt install -y openssh-server

# Install sudo
RUN apt install -y sudo
 
# Set up configuration for SSH
RUN mkdir /var/run/sshd
RUN echo 'root:root' | chpasswd
RUN useradd -ms /bin/bash ansible -g root -G sudo
RUN echo 'ansible:ansible' | chpasswd
RUN sed -i -e '$aPermitRootLogin prohibit-password' /etc/ssh/sshd_config
RUN sed -i -e '$aPermitRootLogin yes' /etc/ssh/sshd_config
RUN sed -i -e '$aPasswordAuthentication yes' /etc/ssh/sshd_config
RUN sed -i -e '$aPort 22' /etc/ssh/sshd_config 
RUN sed -i -e '$aansible ALL=(ALL:ALL) NOPASSWD:ALL' /etc/sudoers
# SSH login fix. Otherwise, user is kicked off after login
RUN sed 's@session\s*required\s*pam_loginuid.so@session optional pam_loginuid.so@g' -i /etc/pam.d/sshd
 
ENV NOTVISIBLE "in users profile"
RUN echo "export VISIBLE=now" >> /etc/profile
 
# Expose the SSH port
EXPOSE 22
 
# Run SSH
CMD ["/usr/sbin/sshd", "-D"]
