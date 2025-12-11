# Use the Default Linux Universal dev container base image
FROM mcr.microsoft.com/devcontainers/universal:2

# Use root for installation
USER root

# Install system updates and required tools
RUN apt-get update && apt-get install -y \
    curl \
    python3 \
    python3-pip \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# Install Node.js LTS version (18.x) + npm
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs

# Install Vue CLI globally
RUN npm install -g @vue/cli @vue/cli-service

# Install Flask globally
RUN pip install Flask

# Expose ports for Flask (5000) and Vue dev server (5173)
EXPOSE 5000 5173

# Keep container running in VS Code
CMD ["sleep", "infinity"]
