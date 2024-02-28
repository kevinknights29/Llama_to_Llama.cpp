# Source: https://micromamba-docker.readthedocs.io/en/latest/quick_start.html
FROM mambaorg/micromamba:1.5.6

# Switch to root to install packages
USER root

# Install system packages
RUN apt-get update \
    && apt-get install --no-install-recommends -y \
    # deps for downloading models
    curl \
    # deps for development
    git \
    # deps for python packages
    build-essential \
    python3-dev \
    gcc

# Copy environment file
COPY --chown=$MAMBA_USER:$MAMBA_USER env.yaml /tmp/env.yaml

# Copy requirements.txt
COPY --chown=$MAMBA_USER:$MAMBA_USER requirements.txt /tmp/requirements.txt

# Install Dependencies
RUN micromamba install -y -n base -f /tmp/env.yaml && \
    micromamba clean --all --yes
