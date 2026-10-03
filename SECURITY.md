# Privacy and Publication Rules

This repository is intentionally sanitized for public use.

## Never publish here

- Names or other identifying participant information
- Personal email addresses or phone numbers
- Street addresses or precise household location
- Private health, financial, legal, or caregiving records
- Credentials, tokens, cookies, authentication files, recovery codes, or secrets
- Live private-network addresses or MAC addresses
- Device serial numbers or unique hardware identifiers
- Real camera images or household interior/exterior imagery
- Exact camera, lock, alarm, or sensor placement when it reveals household security posture
- Local usernames or private filesystem paths
- Raw operational logs containing household-specific identifiers
- Detailed security configuration that would unnecessarily increase attack surface

## Public documentation may include

- Generalized architecture
- Sanitized examples using placeholders
- Bounded test results with identifying details removed
- Design lessons and failure modes
- Methodology, evidence rules, and privacy principles

## Placeholder convention

Use descriptive placeholders instead of real operational values, for example:

- `<LOCAL_DEVICE_IP>`
- `<PRIVATE_CONFIG_PATH>`
- `<CAMERA_A>`
- `<PRIMARY_CAREGIVER>`
- `<BACKUP_CAREGIVER>`

## Evidence discipline

A status response, cached image, network connection, or decoded media stream must not be described as proof of a physical condition unless that condition was actually verified.

Public documentation should clearly distinguish **tested**, **reported**, and **proposed** behavior.

## Release check

Before publishing or updating public material, review it for:

1. PII and participant identity
2. Credentials and authentication artifacts
3. Network and device identifiers
4. Private file paths
5. Household-security details
6. Images or logs containing identifying information
7. Claims that exceed the available evidence
