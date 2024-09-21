# Use the official PostgreSQL image from the Docker Hub
FROM pgautoupgrade/pgautoupgrade:16-alpine

# Set environment variables
ENV POSTGRES_USER=lemmy 
ENV POSTGRES_PASSWORD=password
ENV POSTGRES_DB=lemmy

# Create necessary volumes for persistent data storage
VOLUME ["/var/lib/postgresql/data"]


# Start PostgreSQL server
CMD ["postgres", "-c", "session_preload_libraries=auto_explain", \
     "-c", "auto_explain.log_min_duration=5ms", \
     "-c", "auto_explain.log_analyze=true", \
     "-c", "auto_explain.log_triggers=true", \
     "-c", "track_activity_query_size=1048576"]

# Expose the default PostgreSQL port (5432)
EXPOSE 5432