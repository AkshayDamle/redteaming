# Red Team Notes

Personal notes, checklists, and templates for red team engagements and CTF practice.

Use these notes as a starting point for planning and learning—not as a substitute for written authorization, a defined scope, or an agreed rules-of-engagement document.

## Structure

```
├── [recon/](recon/)          # Reconnaissance techniques and tooling notes
├── [payloads/](payloads/)    # Payload snippets and references
├── [checklists/](checklists/)# Engagement checklists
└── [templates/](templates/)  # Report and engagement templates
```

## Start here

- [Passive reconnaissance](recon/passive-recon.md)
- [Active reconnaissance](recon/active-recon.md)
- [Network testing checklist](checklists/network-pentest.md)
- [Web application testing checklist](checklists/web-app-pentest.md)
- [Engagement scope template](templates/engagement-scope.md)
- [Findings report template](templates/findings-template.md)

## Before testing

Confirm the following before interacting with a target:

- Written authorization from the system owner
- In-scope assets, excluded assets, and an approved testing window
- Named contacts and an emergency stop procedure
- Rules for handling credentials, personal data, and evidence
- A plan to report findings and securely delete sensitive materials

## Disclaimer

For authorized security testing and educational use only. Never test systems you do not own or have explicit permission to assess. Keep examples in isolated labs or approved environments, and do not commit real credentials, personal data, or undisclosed vulnerabilities.
