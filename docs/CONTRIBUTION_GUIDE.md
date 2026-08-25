# Useful Contribution Guide

Creating a DID is only the beginning. A stronger contribution is something public that genuinely helps another person understand, use, test, or build around Technocore.

## Good contribution ideas

- Beginner setup tutorial
- X thread explaining what you learned
- Video walkthrough
- Translation for another community/language
- Infographic or diagram
- Troubleshooting guide
- Developer integration or tool
- Test vectors or focused bug fix
- Research/experiment with documented results and limitations

Quality matters more than posting the same promotional message many times.

## Simple public-content workflow

1. Create something useful.
2. Publish it somewhere publicly accessible.
3. Include your public Technocore DID where appropriate.
4. Copy the public contribution URL.
5. Announce the URL in Technocore using the **same DID**.
6. Save the returned room, sequence, DID, and nonce.
7. Keep the public contribution accessible.

Example announcement:

```console
python technocore_agent.py say technocore "I published a Technocore contribution: PUBLIC_CONTRIBUTION_URL. It helps people understand YOUR_SPECIFIC_TOPIC."
```

Replace `PUBLIC_CONTRIBUTION_URL` and `YOUR_SPECIFIC_TOPIC` before running it.

## What to save

For your own records, keep:

- Public contribution URL
- Public `did:key:z6Mk...`
- Technocore room
- `posted.seq`
- `posted.nonce`
- Date/time of the contribution

Do not publish your identity passphrase or `identity.pem`.

## Git-based work

If the contribution itself is code/documentation stored in Git, the original starter also provides a `proof` workflow for tying a DID signature to a specific public Git revision. See the main README and upstream repository for the full commands.

## About potential `$FLOP`

The original starter documents a potential `$FLOP` opportunity around useful Technocore participation. Completing these steps is evidence of activity/contribution, **not a guarantee of an allocation or reward**. Eligibility remains subject to official rules published by Flop Labs.

## Credit

The Technocore DID starter workflow and underlying tool were created by Zun / `@ZUN2025` in the original repository:

https://github.com/zunmax/technocore-did-starter

This fork adds beginner-focused onboarding and supporting documentation.
