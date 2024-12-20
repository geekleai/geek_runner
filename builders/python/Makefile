# Makefile to build and manage the Docker image

# Variables
IMAGE_NAME := geekrun-python
DOCKERFILE := Dockerfile

.PHONY: all build clean run

# Default target
all: build

# Build the Docker image
build:
	docker build -t $(IMAGE_NAME) -f $(DOCKERFILE) .

# Remove the Docker image
clean:
	docker rmi -f $(IMAGE_NAME)

# Run the Docker container interactively
run:
	docker run -it --rm -v $(shell pwd):/workspace $(IMAGE_NAME)