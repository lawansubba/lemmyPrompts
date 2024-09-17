# lemmy-ui/Dockerfile
FROM dessalines/lemmy-ui:0.19.5

# Expose the default port
EXPOSE 1234

# Set environment variables
ENV LEMMY_UI_LEMMY_EXTERNAL_HOST=${LEMMY_UI_LEMMY_EXTERNAL_HOST}
ENV LEMMY_UI_HTTPS=${LEMMY_UI_HTTPS}
ENV LEMMY_UI_DEBUG=${LEMMY_UI_DEBUG}

# Set the entrypoint
ENTRYPOINT ["/usr/bin/lemmy-ui"]