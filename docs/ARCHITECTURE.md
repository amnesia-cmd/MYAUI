# Architecture

MYAUI is a lightweight browser AI assistant prototype.

## Request flow

Browser UI → Express server → AI provider

The server owns provider credentials and exposes the application-facing API. The browser is responsible for presentation and browser-native interaction such as speech features.

## Security boundary

API credentials belong in server-side environment variables and must never be committed or exposed to browser code. Before a production deployment, add authentication, strict CORS, request validation, rate limiting, and per-user data isolation.
