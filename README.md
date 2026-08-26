# Prime Bridge Media - Coach Relay

GitHub Actions workflow that polls the PBM Coach Telegram bot
(`@pbm_kunal_coach_bot`) every 5 minutes and forwards incoming messages
to the VPS relay at `https://events.kunaldahiya.me/coach-relay/incoming`.

The relay runs on the VPS at `/root/events-tracker/coach/relay.py`
and handles LLM + reply.

## Secrets (set in repo Settings > Secrets > Actions)

| Name | Value |
|---|---|
| `PBM_COACH_BOT_TOKEN` | `8984246119:AAFUWVlDmTZT-W3MmM87rHPGOfbHjaa-V9Q` |
| `COACH_RELAY_SECRET` | `pbm-relay-2026` |
| `VPS_RELAY_URL` | `https://events.kunaldahiya.me/coach-relay` |

## Manual run

Actions > PBM Coach poll-and-forward > Run workflow > Run.

## Latency

Up to 5 minutes between cron ticks. 30-second long-poll per run.
