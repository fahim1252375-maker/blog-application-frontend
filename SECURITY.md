# Security Notes

## Scope

This repository is a frontend-only learning and portfolio demonstration. It is not an authentication service and must not be used to protect real accounts or private data.

## Authentication is simulated

- Registration, login, and session state are handled in the browser.
- User records and session data are stored in LocalStorage, which users and browser scripts can read or modify.
- The current password helper uses a fixed application-wide salt with SHA-256. This is not a password-storage scheme suitable for real accounts: it is fast, uses no per-user random salt, and does not use a password-hashing function such as Argon2id, scrypt, or bcrypt.
- Client-side checks can be bypassed. A browser-only session is not proof of identity and must never authorize access to server resources.
- Demo credentials and sample users are public project data.

**Never enter a real password, API key, payment detail, personal record, or other sensitive information into this demo.**

## Before building real authentication

Use a trusted server-side authentication flow. Store passwords only with a modern password-hashing algorithm (prefer Argon2id; scrypt or bcrypt with appropriate parameters are alternatives), unique random salts, and server-side verification. Enforce authorization on every protected API request. Use secure, HttpOnly, SameSite cookies or another carefully designed token strategy, HTTPS, rate limiting, account recovery controls, and security testing.

The separate [BlogSpace Full-Stack](https://github.com/fahim1252375-maker/blogspace-fullstack) repository contains the API-backed learning implementation; it still requires deployment-specific security review before production use.
