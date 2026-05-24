# XML Information Disclosure

## Severity
Medium

## CVSS
5.3 Medium — AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/A:N

## Affected Endpoints
- /DevMgmt/ProductConfigDyn.xml
- Port 80
- Port 8080

## Description
The printer exposed sensitive configuration information through unauthenticated XML management endpoints.

The endpoint returned:
- Firmware version
- Serial number
- UUID
- Password status
- IPv6 information

without authentication.

## Security Impact
The exposed information could assist attackers in:
- Firmware vulnerability research
- Device profiling
- Network mapping
- Targeted exploitation attempts

## Mitigation
- Require authentication for management endpoints
- Disable unnecessary HTTP services
- Restrict access via ACLs/firewall rules
- Enforce HTTPS-only management access
