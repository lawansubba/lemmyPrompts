# pictrs/Dockerfile
FROM asonix/pictrs:0.5.16

# Expose the default port
EXPOSE 4567

# Set environment variables
ENV PICTRS__API_KEY=${PICTRS_API_KEY}
ENV PICTRS__MEDIA__VIDEO_CODEC=vp9
# Add other environment variables as needed

# Set the entrypoint
ENTRYPOINT ["/usr/local/bin/pict-rs"]

CMD ["run"]

RUN timestamp=$(date +'%Y-%m-%d %H:%M:%S') && echo "Current timestamp: $timestamp"