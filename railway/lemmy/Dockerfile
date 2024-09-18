# Stage 1: Build the Lemmy server
FROM rust:1.80 as builder

WORKDIR /usr/src/lemmy

# Copy the source code
COPY . .

# Build the Lemmy server in release mode
RUN cargo build --release

# Stage 2: Create the runtime image
FROM debian:bookworm-slim

# Install required packages
RUN apt-get update && apt-get install -y \
    libssl-dev \
    libpq-dev \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

# Copy the built server from the builder stage
COPY --from=builder /usr/src/lemmy/target/release/lemmy_server /usr/local/bin/lemmy_server

# Create a user to run the server
RUN useradd -ms /bin/bash lemmy

# Switch to the lemmy user
USER lemmy

# Set environment variable for the Lemmy config path
ENV LEMMY_CONFIG=/config/config.hjson

# Create the config directory and copy the lemmy.hjson file
RUN mkdir -p /config
COPY lemmy.hjson /config/config.hjson

# Expose the port (optional, for documentation)
EXPOSE 8536

# Start the Lemmy server
CMD ["lemmy_server"]
