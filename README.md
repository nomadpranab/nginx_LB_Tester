# Frontend Load Balancer Demo

## Quick Start
docker compose up --build

## Open browser
http://localhost:8080

## Test LB (terminal)
# Single hit
curl -s http://localhost:8080/whoami

# 9 hits - see round-robin
for i in {1..9}; do curl -s http://localhost:8080/whoami; echo; done

# Count distribution across 30 requests
for i in {1..30}; do curl -s http://localhost:8080/whoami; done | sort | uniq -c

# See X-Served-By header
curl -I http://localhost:8080

## Teardown
docker compose down
