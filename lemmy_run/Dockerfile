# syntax=docker/dockerfile:1.9
ARG RUST_VERSION=1.80
ARG CARGO_BUILD_FEATURES=default
ARG RUST_RELEASE_MODE=release 

FROM rust:${RUST_VERSION} AS builder

ARG CARGO_BUILD_FEATURES
ARG RUST_RELEASE_MODE
ARG RUSTFLAGS

WORKDIR /lemmy

COPY . ./

RUN ls -la

RUN cargo build --features "${CARGO_BUILD_FEATURES}" --release
RUN mv target/release/lemmy_server ./lemmy_server

FROM debian:bookworm-slim

RUN apt-get update && apt-get install -y libssl-dev libpq-dev ca-certificates curl && rm -rf /var/lib/apt/lists/*

COPY --from=builder /lemmy/lemmy_server /usr/local/bin

ENV RUST_LOG="warn,lemmy_server=debug,lemmy_api=debug,lemmy_api_common=debug,lemmy_api_crud=debug,lemmy_apub=debug,lemmy_db_schema=debug,lemmy_db_views=debug,lemmy_db_views_actor=debug,lemmy_db_views_moderator=debug,lemmy_routes=debug,lemmy_utils=debug,lemmy_websocket=debug"
ENV RUST_BACKTRACE=full

EXPOSE 8536

ENTRYPOINT ["lemmy_server"]