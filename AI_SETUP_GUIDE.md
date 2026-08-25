# AI-Assisted Setup Guide

If terminal commands are new to you, you can use ChatGPT or another AI assistant to guide you through this repository one step at a time.

## Copy this prompt into your AI assistant

```text
I want to set up this Technocore DID Starter repository:
https://github.com/ntgreatsaini/technocore-did-starter

Please guide me from beginning to end.

First identify the operating system and terminal I am using. Then give me ONLY ONE command at a time. Wait for me to paste the output before giving me the next command.

Help me:
1. Check/install Python 3.12.
2. Check/install Git.
3. Clone the repository.
4. Enter the repository folder.
5. Create a Python virtual environment.
6. Activate it.
7. Install requirements.txt.
8. Verify technocore_agent.py works.
9. Create my DID with the init command.
10. Verify my DID with the did command.
11. Send my first signed message to the lobby.
12. Help me identify the posted room, sequence number, DID and nonce.

Important security rules:
- Never ask me to paste my identity.pem file.
- Never ask me to paste my identity passphrase.
- Never ask me to paste private keys or secrets.
- If an error appears, explain it simply and give me one safe fix at a time.
```

## What you can safely share with an AI

Usually safe to share:

- Python version output
- Git version output
- Normal installation logs
- Error messages after checking that they contain no secrets
- Your public `did:key:z6Mk...`
- Public Technocore room and sequence number

Never share:

- `identity.pem`
- your identity passphrase
- private key material
- passwords, API keys, seed phrases, recovery phrases, or other secrets

## Why use one command at a time?

It prevents beginners from getting lost. Run one command, check the result, then continue. If something fails, fix that step before moving forward.

## If you already know what you are doing

You do not need an AI assistant. Use the main [README](README.md) and the original upstream documentation linked there.
