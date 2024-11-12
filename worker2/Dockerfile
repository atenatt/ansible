# Alpine image to set up ansible
FROM alpine:latest

# Install required packages
RUN apk add --no-cache \
    bash \
    openssh \
    curl

# Set workdir
WORKDIR /worker

# Default command
CMD ["sh"]