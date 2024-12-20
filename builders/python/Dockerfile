FROM python:3.12-slim

# Set environment variables
ENV DEBIAN_FRONTEND=noninteractive \
    PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

# Install required system packages
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        git \
        build-essential \
        curl && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Upgrade pip and install Python LSP server
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir "python-lsp-server[all]"

# Verify installation
RUN git --version && python --version && pylsp --version

# Set the working directory
WORKDIR /workspace

# Default command
CMD ["pylsp"]
