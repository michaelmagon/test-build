FROM ubuntu:latest

# Install required packages
RUN apt-get update && apt-get install -y syslog-ng

# Copy the configuration file
COPY syslog-ng.conf /etc/syslog-ng/syslog-ng.conf

RUN mkdir -p /var/log/syslog-ng

# Expose the Syslog-ng port
EXPOSE 514/udp

# Start Syslog-ng
CMD ["syslog-ng", "--no-caps", "--foreground"]