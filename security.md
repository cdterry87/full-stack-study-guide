# Web Security Study Guide

## 🧩 Beginner Level

- **Q:** What is web security?  
  **A:** The practice of protecting websites and web apps from threats like data breaches, unauthorized access, and code injection.

- **Q:** What is HTTPS?  
  **A:** HyperText Transfer Protocol Secure — uses SSL/TLS encryption to secure data between client and server.

- **Q:** What is SSL/TLS?  
  **A:** Protocols for encrypting network communication to ensure confidentiality and integrity.

- **Q:** Why is HTTPS important?  
  **A:** Prevents man-in-the-middle attacks, protects credentials, and ensures trust via certificates.

- **Q:** What is authentication vs authorization?  
  **A:**

  - **Authentication:** Verifying identity (login)
  - **Authorization:** Checking permissions after authentication

- **Q:** What is a session?  
  **A:** A server-side record that stores user-specific data between requests.

- **Q:** What is a cookie?  
  **A:** A small piece of data stored on the client, often used to maintain sessions.

- **Q:** What is CSRF (Cross-Site Request Forgery)?  
  **A:** An attack where a user is tricked into executing unwanted actions on a web app where they’re authenticated.

- **Q:** How do you prevent CSRF?  
  **A:** Use CSRF tokens in forms, verify request origin, and use `SameSite` cookies.

- **Q:** What is XSS (Cross-Site Scripting)?  
  **A:** Injecting malicious JavaScript into web pages viewed by other users.

- **Q:** How do you prevent XSS?  
  **A:** Escape user input, sanitize HTML, and use frameworks that auto-escape (like Blade or React).

- **Q:** What is SQL Injection?  
  **A:** Inserting malicious SQL into queries to manipulate databases.

- **Q:** How do you prevent SQL Injection?  
  **A:** Use prepared statements and ORM query builders (e.g., Eloquent).

- **Q:** What is password hashing?  
  **A:** Converting plain passwords into irreversible hashes using algorithms like bcrypt or Argon2.

- **Q:** Why should you not use MD5 or SHA1 for passwords?  
  **A:** They’re fast and easily brute-forced — not secure for password storage.

---

## ⚙️ Intermediate Level

- **Q:** What is encryption vs hashing?  
  **A:**

  - **Hashing:** One-way, used for passwords.
  - **Encryption:** Two-way, used for secure data transmission/storage.

- **Q:** What is salting?  
  **A:** Adding random data to a password before hashing to prevent rainbow table attacks.

- **Q:** What is a man-in-the-middle (MITM) attack?  
  **A:** When an attacker intercepts communication between client and server to steal or modify data.

- **Q:** What is CORS?  
  **A:** Cross-Origin Resource Sharing — browser policy controlling resource sharing across domains.

- **Q:** How do you secure APIs with CORS?  
  **A:** Whitelist trusted origins and restrict allowed methods/headers.

- **Q:** What is an access token?  
  **A:** A credential used to authenticate API requests (e.g., JWT, OAuth2 tokens).

- **Q:** What are JWTs?  
  **A:** JSON Web Tokens — self-contained tokens containing user claims, digitally signed for verification.

- **Q:** How do you secure JWTs?  
  **A:** Use short expiration, store securely (not in localStorage), and sign with strong secrets.

- **Q:** What are the risks of storing JWTs in localStorage?  
  **A:** Vulnerable to XSS attacks — attackers can steal the token.

- **Q:** What is rate limiting?  
  **A:** Restricting the number of requests per user/IP to prevent abuse or brute force attacks.

- **Q:** What is a brute-force attack?  
  **A:** Repeatedly trying different password combinations until one succeeds.

- **Q:** How do you prevent brute-force attacks?  
  **A:** Rate limiting, account lockout, and CAPTCHAs.

- **Q:** What is the principle of least privilege?  
  **A:** Users and systems should have only the minimum permissions necessary.

- **Q:** What is input validation?  
  **A:** Checking and sanitizing user input before processing.

- **Q:** What is content security policy (CSP)?  
  **A:** A browser feature that restricts where scripts, images, and other resources can load from.

- **Q:** What is the Same-Origin Policy?  
  **A:** Restricts scripts from interacting with content from a different origin for security.

- **Q:** What is a security header?  
  **A:** HTTP headers that enforce browser security (e.g., `X-Frame-Options`, `Strict-Transport-Security`).

---

## 🧠 Advanced Level

- **Q:** What is OAuth2?  
  **A:** An authorization framework that allows third-party applications to access resources without exposing credentials.

- **Q:** What are the main OAuth2 grant types?  
  **A:** Authorization Code, Client Credentials, Password, and Refresh Token.

- **Q:** What is OpenID Connect?  
  **A:** A layer built on OAuth2 for authentication (user identity).

- **Q:** What is a replay attack?  
  **A:** Reusing a valid request or token to repeat an action.

- **Q:** How do you prevent replay attacks?  
  **A:** Use nonces, timestamps, and short-lived tokens.

- **Q:** What is a timing attack?  
  **A:** Exploiting response time differences to infer sensitive information.

- **Q:** How do you prevent timing attacks?  
  **A:** Use constant-time comparison functions for secrets and hashes.

- **Q:** What are SSRF attacks?  
  **A:** Server-Side Request Forgery — attacker tricks a server into making internal requests.

- **Q:** How do you prevent SSRF?  
  **A:** Validate and whitelist URLs, block internal IP ranges.

- **Q:** What is a directory traversal attack?  
  **A:** Exploiting file path input to access unauthorized directories (e.g., `../../etc/passwd`).

- **Q:** How do you prevent directory traversal?  
  **A:** Use whitelisted paths, sanitize file input, and use realpath validation.

- **Q:** What is RCE (Remote Code Execution)?  
  **A:** An attacker injects and executes code on your server.

- **Q:** How do you prevent RCE?  
  **A:** Never use `eval`, sanitize all input, and keep software up to date.

- **Q:** What is clickjacking?  
  **A:** Tricking users into clicking hidden elements (e.g., framing another site).

- **Q:** How do you prevent clickjacking?  
  **A:** Use `X-Frame-Options: DENY` or `Content-Security-Policy: frame-ancestors 'none'`.

- **Q:** What is SQL Injection via ORM?  
  **A:** Using raw SQL strings in ORM queries without parameter binding.

- **Q:** How can you secure environment variables in Laravel?  
  **A:** Keep `.env` files out of version control and use server-level environment variables for secrets.

- **Q:** What is two-factor authentication (2FA)?  
  **A:** Requires two forms of verification (password + token/app) for login.

- **Q:** What is security through obscurity?  
  **A:** Relying on hidden code or configuration for security — _not_ a real protection method.

- **Q:** How do you secure file uploads?  
  **A:** Validate file type/size, store outside web root, and rename files with unique hashes.

- **Q:** What is dependency scanning?  
  **A:** Automatically checking libraries for known security vulnerabilities.

- **Q:** What is a penetration test?  
  **A:** Authorized simulated attack to find security weaknesses.

- **Q:** What is the difference between white-box and black-box testing?  
  **A:** White-box: tester knows codebase; Black-box: tester simulates an external attacker.

- **Q:** What are security best practices for APIs?  
  **A:** Use HTTPS, validate input, rate-limit requests, require authentication, and log access attempts.

- **Q:** What is a honeypot?  
  **A:** A decoy system set up to attract and analyze attackers.
