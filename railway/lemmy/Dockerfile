FROM dessalines/lemmy:dev

ENV RUST_LOG="warn,lemmy_server=debug,lemmy_api=debug,lemmy_api_common=debug,lemmy_api_crud=debug,lemmy_apub=debug,lemmy_db_schema=debug,lemmy_db_views=debug,lemmy_db_views_actor=debug,lemmy_db_views_moderator=debug,lemmy_routes=debug,lemmy_utils=debug,lemmy_websocket=debug"
ENV RUST_BACKTRACE=full

# Copy your configuration file into the image
COPY lemmy.hjson /etc/lemmy/config.hjson

# Set environment variables if necessary
ENV LEMMY_CONFIG_LOCATION=/etc/lemmy/config.hjson

# Expose the port
EXPOSE 8536

# Entry point (optional if already set in base image)
ENTRYPOINT ["lemmy_server"]