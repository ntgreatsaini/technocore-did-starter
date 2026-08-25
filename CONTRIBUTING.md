# Contributing

Thanks for helping make this beginner guide easier, safer, and more accurate.

This repository is a beginner-focused fork of the original Technocore DID Starter by Zun / @ZUN2025. Please preserve upstream attribution when making changes.

## Good contributions

Useful improvements include:

- clearer beginner instructions;
- verified setup notes for different operating systems or shells;
- troubleshooting fixes based on real errors;
- security improvements;
- translations;
- accessibility improvements;
- examples that explain DIDs and signed messages more clearly;
- fixes or improvements to the underlying Python tool, when tested carefully.

## Before submitting code

Never commit:

- `identity.pem`;
- `*.pem` or `*.key` private-key files;
- passphrases;
- passwords or API keys;
- seed/recovery phrases;
- unrelated personal credentials.

Check your changes before committing:

```console
git status --short
git diff
git diff --cached
git ls-files "*.pem" "*.key"
```

The final command should print nothing.

## Documentation style

Write for someone who may have never used a terminal before:

1. Explain the goal of the step.
2. Give the smallest number of commands needed.
3. Explain what success looks like.
4. Mention common mistakes only when useful.
5. Never encourage users to paste private credentials into an AI assistant or public issue.

## Attribution

Do not remove the original MIT license or the credit to the upstream project:

https://github.com/zunmax/technocore-did-starter

The goal of this fork is to build on that work with easier onboarding, not to present the original tool as newly authored here.
