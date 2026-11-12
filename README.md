# External Network Security Assessment

A practical security engineering project demonstrating
containerized network assessment, Linux administration,
least-privilege design, and evidence-based troubleshooting.

## Project Overview

Designed and deployed an ARM64-based Nmap scanner
using Docker Compose on a Raspberry Pi 5.

The scanner assesses authorized external network
exposure while remaining separated from production
services.

## Technology Stack

- Raspberry Pi 5
- Debian Linux
- Docker and Docker Compose
- Nmap 7.95
- Git and GitHub
- TCP/IP networking

## Security Engineering

- Non-root container execution
- Linux capability restrictions
- Read-only container filesystem
- Dedicated Docker bridge networking
- No inbound published ports
- Controlled, on-demand scanning
- Structured assessment reporting

## Initial Assessment

Scope: 100 commonly used TCP ports on an
authorized external network.

Result: No open TCP ports reported within
the tested scope.

This does not constitute a comprehensive
vulnerability assessment.

## Troubleshooting Experience

Identified and investigated a Docker memory-limit
warning caused by a disabled Linux memory cgroup
controller.

Documented the limitation and deferred remediation
to a planned maintenance window to protect
production availability.

## Skills Demonstrated

Linux Administration | Docker | Network Security |
TCP/IP | Nmap | Troubleshooting | Documentation

## Documentation

- [Deployment Case Study](docs/deployment-case-study.md)
- [Architecture](docs/architecture/README.md)
- [Assessment Methodology](docs/methodology/README.md)

## Security and Privacy

This repository contains sanitized documentation.

Actual network addresses, sensitive configurations,
credentials, and raw assessment reports are excluded.

## Status

Initial deployment and baseline assessment completed.
Further hardening and assessment automation planned.
