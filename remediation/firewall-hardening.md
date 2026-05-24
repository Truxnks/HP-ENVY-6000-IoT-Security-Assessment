# Firewall Hardening Recommendations

## Objective
Reduce exposure of insecure printer services on the local network.

## Recommended Actions

### Block IPP Service (TCP/631)

PowerShell:
```powershell
New-NetFirewallRule -DisplayName "Block Printer IPP" `
-Direction Inbound `
-Protocol TCP `
-LocalPort 631 `
-Action Block
