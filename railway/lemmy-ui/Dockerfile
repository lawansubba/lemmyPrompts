# lemmy-ui/Dockerfile
FROM dessalines/lemmy-ui:0.19.5

# Set environment variables
ENV LEMMY_UI_LEMMY_INTERNAL_HOST=lemmy.railway.internal:8536

ENV LEMMY_UI_LEMMY_EXTERNAL_HOST=localhost:1237

ENV LEMMY_UI_HTTPS=false 

ENV LEMMY_UI_DEBUG=true

# Print the environment variable during build
RUN echo "LEMMY_UI_LEMMY_INTERNAL_HOST: $LEMMY_UI_LEMMY_INTERNAL_HOST"