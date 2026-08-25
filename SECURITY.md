# Security Guide

Your Technocore DID is public. Your private identity is not.

## Public — safe to share

- Your `did:key:z6Mk...` DID
- Public contribution URLs
- Technocore room names
- Server-assigned sequence numbers
- Public message text

## Private — never share

- `identity.pem`
- Your identity passphrase
- Private key material
- Passwords, API keys, seed phrases, recovery phrases, or unrelated secrets

The repository `.gitignore` excludes `*.pem` and `*.key` files to reduce the chance of accidentally committing private keys. Always check `git status` before committing anyway.

## Back up your identity

After creating your DID, securely back up `identity.pem` and keep its passphrase separately. Do not put either one in a public repository.

## Using ChatGPT or another AI assistant

AI can help interpret normal terminal output and errors, but never paste `identity.pem`, its contents, your passphrase, or any private key into an AI conversation.

When asking for troubleshooting help, share only the command you ran and sanitized output.

## Before a Git commit

Run:

```console
git status --short
git diff --cached --name-only
git ls-files "*.pem" "*.key"
```

The last command should print nothing. If it prints a private-key file, stop and remove that file from Git tracking before committing.

## If a private key is exposed

Treat the exposed identity as compromised. Do not rely on deleting a public commit as proof that the secret was never copied. Create a new identity and stop using the exposed private identity for future activity.
