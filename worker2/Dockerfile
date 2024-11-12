# Dockerfile for Worker 2
FROM alpine:latest

# Install required packages
RUN apk add --no-cache \
    bash \
    openssh \
    curl

# Set workdir
WORKDIR /worker

# Default command: Add public key to authorized_keys and start the container
CMD /bin/sh -c "mkdir -p /root/.ssh && cat /ansible/ssh/id_rsa.pub >> /root/.ssh/authorized_keys && tail -f /dev/null"
