# Use the default Linux Universal Image
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# Set the working directory
WORKDIR /workspace

# Install basic utilities
RUN apt-get update && apt-get install -y \
    curl \
    git \
    build-essential \
    python3 \
    python3-pip \
    python3-venv \
    nodejs \
    npm

# Install Vue.js (Node.js package manager for Vue)
RUN npm install -g @vue/cli

# Install Flask (Python web framework)
RUN pip3 install flask

# Expose the necessary ports (default for Vue and Flask apps)
EXPOSE 8080
EXPOSE 5000

# Create a Python virtual environment
RUN python3 -m venv /workspace/.venv

# Ensure the virtual environment is activated and install Flask
RUN /workspace/.venv/bin/pip install --upgrade pip
RUN /workspace/.venv/bin/pip install flask
