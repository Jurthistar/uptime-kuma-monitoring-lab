# Alert-Test Record

## Objective

Verify that an outage is detected and that the selected notification service sends both failure and recovery messages.

## Test setup

| Field | Value |
|---|---|
| Monitor | Alert test |
| Monitor type | HTTP(S) |
| Test target | `https://example.invalid` |
| Notification channel | Telegram |
| Test date | 2026-09-06 |

## Procedure

1. Create the monitor using the invalid test URL.
2. Attach the notification channel.
3. Wait for Uptime Kuma to mark it as **Down**.
4. Capture the failed state and the notification. Hide channel names, email addresses, message IDs, and webhook details.
5. Pause the monitor or change its URL to a valid one.
6. Confirm that a recovery notification arrives.

## Result

> The monitor detected the planned failure and sent a Telegram failure notification. After the target was restored to a valid URL, Telegram sent a recovery message. This verified the end-to-end alerting workflow.

## Evidence

Add your cleaned screenshot as `screenshots/03-alert-test.png`.
