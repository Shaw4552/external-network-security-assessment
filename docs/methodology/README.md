# External Network Assessment Methodology

## 1. Authorization

Assess only networks and systems for which
explicit authorization has been established.

## 2. Scope

Initial assessment:

- One authorized public IPv4 address
- 100 commonly used TCP ports
- No exploitation
- No credential testing
- No UDP scanning

## 3. Assessment Configuration


The initial assessment used the following Nmap options:

| Option | Purpose |
|---|---|
| `-Pn` | Skip host discovery |
| `-sT` | TCP connect scan |
| `-T2` | Conservative timing |
| `--top-ports 100` | Test 100 common TCP ports |
| `--open` | Display open or potentially open ports |
| `--reason` | Show available port-state reasons |
| `-oA` | Save multiple report formats |

## 4. Verification

1. Confirm target authorization and current public IP.
2. Verify scanner public egress.
3. Inspect the external route.
4. Verify report permissions.
5. Record scan completion and preserve evidence.

## 5. Initial Results

The scan completed successfully.

No open TCP ports were reported among the
100 tested ports.

## 6. Limitations

- Not a full TCP-port assessment
- UDP not assessed
- No vulnerability testing performed
- `-Pn` assumes the target is up
- `--open` suppresses non-open port details
- Results represent a point-in-time observation

## 7. Evidence Management

Store raw reports outside public Git repositories.

Preserve original reports, timestamps, scope,
and scan configurations in access-controlled storage.

## 8. Planned Improvements

- Timestamped reporting
- Full TCP-port assessment
- Selected UDP scanning
- Automated result comparison
- Remediation tracking
