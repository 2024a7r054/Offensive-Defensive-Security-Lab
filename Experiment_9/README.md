# Experiment 9: Authentication Security Review

## Aim

Review the risks of repeated password guesses and identify defensive controls that reduce account compromise.

## Scope and safety

This report summarizes an authorized lab exercise at a high level. It does not include password-guessing commands, target details, wordlists, or recovered credentials. The source screenshots were omitted because they exposed live guessing output and credential material.

## Defensive review

Assess authentication protections through configuration review and approved audit logs. Useful controls include:

- Multi-factor authentication for user and administrator accounts.
- Rate limits, progressive delays, and temporary lockouts for repeated failures.
- Monitoring and alerting for unusual failed-login volume and successful logins after repeated failures.
- Unique, long passwords stored with a modern password-hashing scheme.
- A documented response process for suspected credential exposure, including password resets and session revocation.

## Result

The original lab report documented a successful password-guessing outcome. No target identifiers or recovered credentials are reproduced here. Treat any credentials used in a lab as compromised and rotate them before reusing the environment.

## Conclusion

Authentication testing should be authorized, tightly scoped, and coordinated with the system owner. Defensive monitoring, strong authentication, and rate limiting reduce the likelihood and impact of password guessing.

Adapted with permission from [4316sushil39's source repository](https://github.com/4316sushil39/Offensive-and-defensive-security-COM-502-/tree/main/Exp-9). Operational instructions and credential-bearing screenshots were intentionally excluded.
