# Monitor Inventory

Replace the **Status** column after you create and test each monitor.

| Monitor name | Type | Target | Interval | Expected result | Status |
|---|---|---|---:|---|---|
| GitHub availability | HTTP(S) | `https://github.com` | 60 seconds | Available / HTTP 200-range response | Tested — operational |
| Portfolio availability | HTTP(S) | Your public portfolio URL | 60 seconds | Available | Tested — operational |
| Cloudflare DNS reachability | Ping | `1.1.1.1` | 60 seconds | Replies received | Tested — operational |
| Alert test | HTTP(S) | Controlled invalid URL, then a valid URL for recovery | 60 seconds | Down and recovery notifications through Telegram | Tested — operational |

## Why these checks

- **HTTP(S)** verifies that a website can be reached over the web, not merely that a device is online.
- **Ping** provides a simple reachability check for a public network endpoint.
- **Alert test** deliberately creates a controlled failure so the notification path can be proven.

## Notes

Do not add private hostnames, local IP addresses, router names, or credentials to this public repository. If you monitor internal devices, document them generically (for example, “Home-lab service”) or omit them altogether.
