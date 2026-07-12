PRIVATE-SETUP VERSION

No username, password, password hash, or fixed salt is embedded in the GitHub source.

On first launch on a device:
1. The user creates a username and password.
2. A cryptographically random 128-bit salt is generated locally.
3. The username verifier is SHA-256(salt || username).
4. The password derives an AES-256-GCM key using PBKDF2-HMAC-SHA-256 with 600,000 iterations.
5. Tracker data is encrypted locally with AES-256-GCM.
6. Only the salt, username verifier, IV, and ciphertext are stored in the browser.

Important:
- GitHub Pages remains a public static site.
- Anyone can view the application code, but no credential is present in it.
- A visitor on another device receives a separate empty local vault.
- A weak password such as "ggwp" can still be guessed offline. Use a long unique passphrase.
- For true server-side access restriction, use Cloudflare Access, Firebase Authentication,
  or another authenticated backend.
