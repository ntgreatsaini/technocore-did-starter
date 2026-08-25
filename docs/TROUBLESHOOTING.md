# Troubleshooting

The safest way to troubleshoot is one step at a time. Do not keep running later commands when an earlier step failed.

## `python`, `python3`, or `py` is not recognized

Python is either not installed, the wrong version is installed, or your shell cannot find it. Install Python 3.12 using the supported method for your system, reopen the terminal, and verify it again.

If you use an AI assistant, tell it your operating system, terminal, and the exact error. Do not send secrets.

## `git` is not recognized

Install Git, reopen the terminal, and run:

```console
git --version
```

Continue only after Git responds with a version.

## Virtual environment will not activate

Activation commands differ between PowerShell, Command Prompt, bash, and zsh. Use the matching section in the main README.

For PowerShell, if script execution blocks activation, the upstream guide documents a process-scoped execution-policy workaround. Do not permanently weaken system security just to activate a virtual environment.

## `ModuleNotFoundError` or `cryptography` missing

Make sure `.venv` is activated and run:

```console
python -m pip install -r requirements.txt
```

Then retry:

```console
python technocore_agent.py --version
```

## I closed the terminal and `(.venv)` disappeared

That is normal. Return to the repository directory and activate `.venv` again. You do not need to recreate your DID.

## I already created a DID

Do **not** run `init` again just to view it. Run:

```console
python technocore_agent.py did
```

Enter the existing identity passphrase locally.

## Wrong passphrase / identity will not open

Check that you are using the correct `identity.pem` and passphrase. Do not paste either into a public issue, chat, screenshot, or AI assistant.

## My `say` command returned lots of JSON

Look near the end for the `posted` object. Save its room/sequence/DID/nonce information. The `from` value should be the public DID that signed your message.

## I need AI help

Use [AI_SETUP_GUIDE.md](../AI_SETUP_GUIDE.md). Paste the provided prompt into ChatGPT or another AI assistant, then give it sanitized terminal output one command at a time.

Never provide an AI with:

- `identity.pem`
- your passphrase
- private keys
- seed/recovery phrases
- passwords or API keys

## Still stuck?

Read the original upstream repository documentation at https://github.com/zunmax/technocore-did-starter and compare your step with the documented commands for your environment.
