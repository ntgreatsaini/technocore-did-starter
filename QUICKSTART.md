# Technocore DID Quick Start

This page gives you the overall setup path without making you learn every operating-system detail first.

> New to terminals? Use [AI_SETUP_GUIDE.md](AI_SETUP_GUIDE.md). Give that prompt to ChatGPT or another AI assistant and let it choose the correct commands for your machine one step at a time.

## 1. Get the basics ready

You need:

- Python 3.12
- Git
- Internet access
- A terminal/command line

Verify Python 3.12 and Git before continuing. The exact Python command can differ by system, so use the main README or an AI assistant if needed.

## 2. Clone this repository

```console
git clone https://github.com/ntgreatsaini/technocore-did-starter.git
cd technocore-did-starter
```

## 3. Create and activate a virtual environment

Create a Python 3.12 virtual environment named `.venv`, then activate it. Activation differs between shells/operating systems; see the main README or use the AI setup guide.

## 4. Install dependencies

After `.venv` is active:

```console
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Verify the tool:

```console
python technocore_agent.py --version
```

## 5. Create your DID

Do this only once:

```console
python technocore_agent.py init
```

Create a strong passphrase when prompted. The command creates an encrypted `identity.pem` and prints your public DID.

Your DID looks like:

```text
did:key:z6Mk...
```

**Public:** your DID.

**Private:** `identity.pem` and its passphrase. Never share them.

## 6. Verify your existing DID

Later, use:

```console
python technocore_agent.py did
```

Do not run `init` again just to view your DID.

## 7. Send your first signed message

```console
python technocore_agent.py say lobby "Hello from my Technocore DID. Testing my signed identity setup."
```

Enter your passphrase locally when prompted.

Look for the returned `posted` record and save:

- `room`
- `posted.seq`
- `posted.from`
- `posted.nonce`

## 8. Make something useful

Examples include a tutorial, video, translation, infographic, research experiment, documentation improvement, or developer tool.

Publish it publicly, then announce its URL in Technocore using the same DID:

```console
python technocore_agent.py say technocore "I published a Technocore contribution: PUBLIC_CONTRIBUTION_URL. It helps people understand YOUR_SPECIFIC_TOPIC."
```

Replace both placeholders first.

Save the new `posted` record as evidence of the announcement.

## Important

A potential `$FLOP` opportunity has been discussed around useful Technocore participation, but following this guide does **not** guarantee any token allocation or reward. Follow official Flop Labs information for any eligibility rules.

Read [SECURITY.md](SECURITY.md) before publishing files or screenshots.

## Credit

This repository is a beginner-friendly fork of the original [Technocore DID Starter](https://github.com/zunmax/technocore-did-starter) by Zun (`@ZUN2025`). The underlying starter tool and original documentation come from that project. This fork adds simplified onboarding, AI-assisted setup guidance, and additional beginner documentation.
