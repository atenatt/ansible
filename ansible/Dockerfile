# Dockerfile for Ansible
FROM alpine:latest

# Install dependencies
RUN apk add --no-cache \
    ansible \
    openssh \
    python3 \
    py3-pip \
    bash \
    && python3 -m venv /opt/venv \
    && . /opt/venv/bin/activate \
    && pip install --no-cache-dir --upgrade pip ansible

# Ensure virtual environment activation
ENV PATH="/opt/venv/bin:$PATH"

# Set work directory
WORKDIR /ansible

# Default command
CMD ["ansible-playbook", "--version"]