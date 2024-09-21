# lemmy-ui/Dockerfile
FROM dessalines/lemmy-ui:0.19.5

# Set environment variables
ENV LEMMY_UI_LEMMY_INTERNAL_HOST=lucid-eagerness.railway.internal

# Print the environment variable during build
RUN echo "LEMMY_UI_LEMMY_EXTERNAL_HOST: $LEMMY_UI_LEMMY_EXTERNAL_HOST"

# Set the entrypoint
ENTRYPOINT ["/usr/bin/lemmy-ui"]