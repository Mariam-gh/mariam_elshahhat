FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Install extra packages
RUN apt-get update && apt-get install -y xz-utils

# -------------------------
# Install Vue.js
# -------------------------
# Install Vue CLI globally
RUN npm install -g @vue/cli @vue/cli-service

# -------------------------
# Install Flask
# -------------------------
RUN pip install Flask

# Expose common dev ports
EXPOSE 5000 5173

# Keep container running
CMD ["sleep", "infinity"]
