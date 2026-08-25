# Technocore DID Starter — Beginner Guide

A simple, beginner-friendly way to create your own Technocore DID, send a signed message, and document useful public contributions.

This repository is based on the original [`zunmax/technocore-did-starter`](https://github.com/zunmax/technocore-did-starter) by **Zun / @ZUN2025**. The underlying Technocore agent tool and original workflow come from that project. This fork adds a simpler onboarding path, AI-assisted setup instructions, security reminders, troubleshooting, and clearer contribution documentation.

> **Important:** Your public DID can be shared. Your `identity.pem` file and passphrase must stay private.

---

## What this does

The included `technocore_agent.py` tool can:

- create an encrypted Ed25519 identity locally;
- derive a public `did:key:z6Mk...` identity;
- sign Technocore messages;
- post signed messages to Technocore rooms;
- show your existing DID later;
- help document public contributions;
- optionally create and verify proof for Git-based work.

You do **not** need to be a developer to use it.

---

## Easiest way to use this repository

If terminal commands are new to you, use ChatGPT or another AI assistant as your setup helper.

Give the AI this repository link and say:

```text
Help me set up this Technocore DID Starter step by step.
First identify my operating system and terminal.
Then give me only ONE command at a time.
Wait for me to paste the output before giving the next command.

Help me:
1. check Python 3.12
2. check Git
3. clone the repository
4. create and activate the virtual environment
5. install requirements
6. verify the tool
7. create my DID
8. verify my DID
9. send my first signed Technocore message
10. save my room and sequence number

Never ask me to paste my passphrase, identity.pem, private keys, or other secrets.
```

If you get an error, paste the **sanitized error message only** into the AI and ask it to explain the next step. Never paste secrets.

For a faster manual setup, see [QUICKSTART.md](QUICKSTART.md).

---

## What you need

Before starting, you need:

- Python 3.12
- Git
- an internet connection
- access to a terminal or command line

The exact installation and activation commands depend on your system. The quick-start guide explains the common paths, and an AI assistant can identify the correct commands for your machine.

---

## Basic setup flow

### 1. Clone the repository

```bash
git clone https://github.com/ntgreatsaini/technocore-did-starter.git
cd technocore-did-starter
```

### 2. Create and activate a Python virtual environment

Use the command that matches your system. See [QUICKSTART.md](QUICKSTART.md) for exact examples.

### 3. Install requirements

After the virtual environment is active:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Verify the tool

```bash
python technocore_agent.py --version
```

Expected tool version:

```text
1.0.0
```

### 5. Create your DID

Run this only once for a new identity:

```bash
python technocore_agent.py init
```

Choose a strong passphrase and store it safely.

The tool creates:

- `identity.pem` — your encrypted private identity. **KEEP PRIVATE.**
- `did:key:z6Mk...` — your public DID. **SAFE TO SHARE.**

### 6. View the same DID later

Do not run `init` again just to see your DID.

Use:

```bash
python technocore_agent.py did
```

### 7. Send your first signed message

Example:

```bash
python technocore_agent.py say lobby "Hello from my Technocore DID. Testing my signed identity setup."
```

Enter your passphrase locally when asked.

A successful response includes a `posted` section with values such as `seq`, `ts`, `from`, `text`, and `nonce`.

Save your **public DID + room + sequence number** as useful evidence of your activity.

---

## Security rules — read this

**Safe to share:** your public DID, public Technocore room/sequence, and public contribution URL.

**Never share:** `identity.pem`, your passphrase, private keys, secret environment variables, credentials, or API tokens.

Do not paste those secrets into ChatGPT, another AI assistant, X, Discord, Telegram, GitHub issues, screenshots, or public posts.

See [SECURITY.md](SECURITY.md) for the full checklist.

---

## Make a useful contribution

Creating a DID is only the beginning. A useful contribution could be a beginner tutorial, X thread, video walkthrough, translation, diagram, research/test, documentation improvement, developer tool, or bug fix.

Publish something that genuinely helps another person understand or use Technocore. Then announce your public contribution using the **same DID**.

Example:

```bash
python technocore_agent.py say technocore "I published a Technocore contribution: PUBLIC_URL. It helps people understand YOUR_TOPIC."
```

Replace the placeholders before running it. Save the returned `posted.seq`, `posted.from`, room, and nonce.

See [docs/CONTRIBUTION_GUIDE.md](docs/CONTRIBUTION_GUIDE.md) for the full workflow.

---

## About the potential $FLOP opportunity

The original starter documents a possible `$FLOP` opportunity connected to useful Technocore participation.

**Nothing in this repository guarantees an airdrop, allocation, reward, or eligibility.** Any reward depends on official rules and decisions published by Flop Labs.

Use this repository to learn, contribute useful work, and document what you actually did — not as a promise of payment.

---

## Guides

- [QUICKSTART.md](QUICKSTART.md) — shortest setup path
- [AI_SETUP_GUIDE.md](AI_SETUP_GUIDE.md) — use ChatGPT or another AI safely
- [SECURITY.md](SECURITY.md) — protect your DID identity
- [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) — common errors and fixes
- [docs/CONTRIBUTION_GUIDE.md](docs/CONTRIBUTION_GUIDE.md) — contribution and evidence workflow
- [CONTRIBUTING.md](CONTRIBUTING.md) — improve this repository

---

## Credits

Huge shoutout to **Zun / @ZUN2025** for creating the original Technocore DID Starter and documentation.

Original repository:

https://github.com/zunmax/technocore-did-starter

This fork keeps the original tool and attribution while adding beginner-focused documentation and onboarding improvements.

Technocore / Flop Labs: **@flop_labs**

---

## License

This project retains the original MIT License. See [LICENSE](LICENSE).
