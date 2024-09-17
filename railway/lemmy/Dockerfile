# lemmy/Dockerfile
FROM dessalines/lemmy:0.19.5

# Copy the configuration file
COPY lemmy.hjson /config/config.hjson

# Expose the default port
EXPOSE 8536

# Set the entrypoint
ENTRYPOINT ["/usr/bin/lemmy_server"]