# lemmy-ui/Dockerfile
FROM dessalines/lemmy-ui:dev

# Set environment variables
ENV LEMMY_UI_LEMMY_INTERNAL_HOST=lemmy-test.up.railway.app

ENV LEMMY_UI_LEMMY_EXTERNAL_HOST=lemmyui-test.up.railway.app

ENV LEMMY_UI_HTTPS=true 

ENV LEMMY_UI_DEBUG=true

RUN timestamp=$(date +'%Y-%m-%d %H:%M:%S') && echo "Current timestamp: $timestamp"