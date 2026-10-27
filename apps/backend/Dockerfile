FROM gcc:13-bookworm AS builder

WORKDIR /src

COPY . .

RUN make -C lib && make -C apps/backend

FROM debian:bookworm-slim

WORKDIR /app

COPY --from=builder /src/apps/backend/backend /app/backend

EXPOSE 9000

ENTRYPOINT ["/app/backend"]