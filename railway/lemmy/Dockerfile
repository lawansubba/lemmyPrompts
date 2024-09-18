FROM dessalines/lemmy:dev

# Copy your configuration file into the image
COPY lemmy.hjson /etc/lemmy/config.hjson

# Set environment variables if necessary
ENV LEMMY_CONFIG_LOCATION=/etc/lemmy/config.hjson

# Expose the port
EXPOSE 8536

# Entry point (optional if already set in base image)
ENTRYPOINT ["lemmy_server"]