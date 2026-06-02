FROM debian:12

RUN apt update && apt install -y \
    openssh-server \
    sudo \
    python3 \
    python3-apt \
    curl \
    iproute2 \
    systemctl \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -m -s /bin/bash ansible \
    && echo "ansible:ansible" | chpasswd \
    && usermod -aG sudo ansible \
    && echo "ansible ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ansible

RUN mkdir -p /run/sshd

EXPOSE 22 80 443 3306

CMD ["/usr/sbin/sshd", "-D"]
