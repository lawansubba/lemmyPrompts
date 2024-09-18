# Use the official Rust image as the base image
FROM rust:1.70 as builder

# Set the working directory
WORKDIR /app

# Copy the source code into the container
COPY . .

# Build the application
RUN cargo build --release

# Create a new stage with a minimal image
FROM debian:bullseye-slim

# Install necessary dependencies
RUN apt-get update && apt-get install -y libssl-dev libpq-dev ca-certificates && rm -rf /var/lib/apt/lists/*

# Copy the built binary from the builder stage
COPY --from=builder /app/target/release/lemmy_server /usr/local/bin/lemmy_server

# Set the entrypoint
ENTRYPOINT ["lemmy_server"]

# Expose the port Lemmy runs on
EXPOSE 8536

# Use SIGTERM as the stop signal
STOPSIGNAL SIGTERM