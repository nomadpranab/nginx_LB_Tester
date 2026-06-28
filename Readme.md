Frontend + Docker + Nginx LB
Complete Notes — Architecture, Commands & LB Testing
Static Site  |  Docker  |  Nginx Reverse Proxy  |  Load Balancer  |  Interview Q&A
Covers: Project structure · Dockerfile · Nginx config · docker-compose · LB algorithms · Testing LB with commands + expected output · Interview Q&A

SECTION 1 — Project Architecture

A frontend-only project has no Node.js server, no Python — just static files (HTML, CSS, JS). Nginx inside Docker is the perfect server for this. We then run 3 identical replicas of this Nginx container and put a 4th Nginx container in front as a Load Balancer.

