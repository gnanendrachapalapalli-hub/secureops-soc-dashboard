# secureops-soc-dashboard
soc, cybersecurity, siem, dashboard, incident-response, threat-intelligence, javascript, html-css, rbac, mitre-attack
# SecureOps SOC Dashboard

A browser-based Security Operations Center console. It shows how a SOC analyst's shift flows from live telemetry to triage to incident response to reporting.

All data is simulated. There is no backend, and nothing leaves the browser.

**Live demo:** <your GitHub Pages link>

## Demo accounts

| Username | Password | Role |
|---|---|---|
| analyst | analyst123 | Analyst |
| manager | manager123 | Manager |
| admin | admin123 | Admin |

Two-factor is optional on the login page. Enter any 6 digits.

## Features

- **Real-time view:** events per second chart (60s window), threat level gauge, security posture ring, live event stream with severity filter, attack origins, IOC hits
- **Alerts:** search and filter by severity, status and type. Acknowledge, close, view detail, export CSV
- **Incidents:** create, assign owners, add timeline notes, change status
- **Network:** topology diagram and active flows. Isolate hosts, block IPs, add to watchlist, capture PCAP
- **Threat intel:** look up an IP, domain or hash across four simulated sources, then raise an incident from the result
- **MITRE ATT&CK:** alert counts per kill chain phase, click a technique to filter alerts
- **Playbooks, reports, settings, user management**
- **Role-based access:** analysts triage, managers close incidents and run playbooks, admins manage users
- **Sign up and login** with validation, password strength meter, duplicate username check
- **Dark and light themes**, responsive down to phone width

## Tech

Plain HTML, CSS and JavaScript in one file. No framework, no build step, no dependencies except Google Fonts.

- CSS custom properties for theming
- Charts drawn as inline SVG from JavaScript
- One reusable modal and one reusable dropdown for every dialog
- A single `setInterval` loop drives the live data

## Run locally

Open `index.html` in a browser.

## Limits

- Data resets on refresh
- Passwords are stored in memory only. This is a UI demo and is not a real authentication system
- Threat intel verdicts are generated, not fetched from real services

## Possible next steps

Node.js backend with a real database, WebSocket event feed, JWT authentication, real integrations (AbuseIPDB, VirusTotal).
