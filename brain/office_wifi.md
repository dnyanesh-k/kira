# Office WiFi Setup Guide

## Networks

| Network | Purpose | Password |
|---------|---------|----------|
| CorpNet-5G | Employees only — use this | Ask IT: ext 4422 |
| CorpNet-Guest | Visitors only — no access to internal apps | Welcome@Guest23 |
| CorpNet-IoT | Printers and devices only — do not connect laptops | N/A |

**Do NOT connect to CorpNet-Guest** on your work laptop — it blocks access to all internal tools (Jira, Confluence, HR portal).

## First-time Setup (Windows)

1. Click WiFi icon → select **CorpNet-5G**
2. Authentication type: **WPA2-Enterprise**
3. Username: your employee email (e.g. `john.doe@corp.internal`)
4. Password: your SSO password (same as laptop login)
5. Certificate: select **CorpCA-2024** from the dropdown — if missing, run `certutil -addstore Root \\fileserver\it\CorpCA-2024.cer`

## First-time Setup (Mac)

1. Click WiFi → **CorpNet-5G**
2. Enter username: `john.doe@corp.internal`, password: SSO password
3. When prompted to verify certificate, click **Trust** — it should show issuer: `CorpCA Internal Root 2024`

## Common Issues

**"Authentication failed"**
Your SSO password may have expired. Reset at `https://sso.corp.internal/reset` before reconnecting.

**Connected but can't reach Jira / internal sites**
You're likely on CorpNet-Guest. Disconnect and reconnect to CorpNet-5G.

**Certificate missing on new laptop**
Run: `\\fileserver.corp.internal\it\scripts\install_cert.bat` — requires VPN if off-site.

## Off-site / VPN

When working from home: connect to VPN first at `vpn.corp.internal` using Cisco AnyConnect,
then all internal sites work over your home internet. WiFi setup is office-only.
