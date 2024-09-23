# lemmy-ui/Dockerfile
FROM dessalines/lemmy-ui:dev

# Set environment variables
ENV LEMMY_UI_LEMMY_INTERNAL_HOST=lemmy.railway.internal

#ENV LEMMY_UI_LEMMY_EXTERNAL_HOST=localhost:1236

ENV LEMMY_UI_HTTPS=false 

ENV LEMMY_UI_DEBUG=true

# Print the environment variable during build
RUN echo "LEMMY_UI_LEMMY_INTERNAL_HOST: $LEMMY_UI_LEMMY_INTERNAL_HOST"