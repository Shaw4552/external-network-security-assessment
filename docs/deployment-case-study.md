# External Network Security Scanner — Deployment Case Study

Date: 2026-11-12
Status: Initial deployment validated

## Objective

Deploy a dedicated, least-privilege ARM64 Nmap container
for authorized external network exposure assessments.

## Technology

- Raspberry Pi 5
- Debian Linux
- Docker Engine and Compose
- Nmap 7.95
- Git and GitHub

## Security Architecture

- Non-root execution
- Dropped Linux capabilities
- Read-only root filesystem
- No published inbound ports
- Dedicated report storage
- On-demand execution

## Validation

- ARM64 container built successfully
- Public internet egress verified
- Independent external routing verified
- Report writing verified
- Initial top-100 TCP assessment completed
- No open TCP ports reported in the tested scope

## Troubleshooting

Identified a Docker memory-limit warning.

Root cause: the host boot configuration contains
`cgroup_disable=memory`.

The memory limit is not enforced. Remediation is
deferred to planned host maintenance.

A separate investigation confirmed that the Linux
host had not rebooted when Docker containers
recently restarted.

## Assessment Limitations

The initial assessment did not include full TCP
coverage, UDP scanning, or vulnerability testing.

Results do not establish that the target network
is free of vulnerabilities.

## Lessons Learned

- Verify configured container security controls.
- Distinguish service uptime from host uptime.
- Preserve production availability during testing.
- Document assessment scope and limitations.
- Keep raw security reports outside public Git.
