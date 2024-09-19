# Use the official PostgreSQL image from the Docker Hub
FROM postgres:16-alpine

# Set environment variables
ENV POSTGRES_USER=lemmy
ENV POSTGRES_PASSWORD=password
ENV POSTGRES_DB=lemmy

# Add custom configuration if needed (optional)
# You can copy a custom config file into the image like this:
# COPY ./custom-postgresql.conf /etc/postgresql/postgresql.conf

# Expose the default PostgreSQL port (5432)
EXPOSE 5432

# Start PostgreSQL server
CMD ["postgres", "-c", "session_preload_libraries=auto_explain", \
     "-c", "auto_explain.log_min_duration=5ms", \
     "-c", "auto_explain.log_analyze=true", \
     "-c", "auto_explain.log_triggers=true", \
     "-c", "track_activity_query_size=1048576"]