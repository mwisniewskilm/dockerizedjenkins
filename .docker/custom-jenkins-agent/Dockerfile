FROM jenkins/ssh-agent:jdk11

USER root

# Update package lists and install OpenJDK 17, PHP, curl, and unzip
RUN apt-get update && \
    apt-get install -y openjdk-17-jdk php-cli php-zip php-mbstring curl unzip && \
    rm -rf /var/lib/apt/lists/*

# Install Composer globally
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Set the JAVA_HOME environment variable to the location of OpenJDK 17
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64

# Update the PATH to include Java binaries
ENV PATH="$JAVA_HOME/bin:$PATH"

# Verify installation of curl, php, and composer (optional for debugging purposes)
RUN curl --version && php --version && composer --version
