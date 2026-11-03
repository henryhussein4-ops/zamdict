# Security

ZamDict is beta software. Please do not use it for sensitive or confidential information.

## Reporting a security concern

Do not publish exploitable details or credentials in a public issue. Until a private reporting channel is configured for this repository, contact the maintainer through their GitHub profile and request a private disclosure route. Include steps to reproduce and the potential impact, but do not send secrets or personal data.

## Credential handling

- Never commit provider API keys or other credentials.
- The public release contains no embedded Groq API key. AI testing requires a user-supplied key, saved in that browser's local storage and sent directly from the browser to Groq. This is a convenience for local testing, not a secure production architecture.
- Do not use production or high-value credentials in this client-side app. A production deployment should put provider credentials behind a trusted server-side proxy and apply rate limits and monitoring.
- The existing Firebase endpoint and backend rules have not been audited as part of this release preparation. Review database access, privacy, and abuse protections before production use.
