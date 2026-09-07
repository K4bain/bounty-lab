# Bounty Lab

Autonomous bounty workspace driven by the Internal AI Entity.

- Entity (https://entity-production-097d.up.railway.app) qualifies open bounties from Algora/Polar
- Matched issues get created here with the 'openhands' label
- OpenHands Resolver GitHub Action attempts fixes autonomously
- PRs come back for owner review - owner merges and collects

## Flow
1. Entity scans Algora hourly (n8n cron + entity webhook)
2. Entity creates task + issue here with full repo analysis
3. Resolver Action (workflow_run) attempts the fix with an LLM
4. PR draft appears; entity pings owner for review

