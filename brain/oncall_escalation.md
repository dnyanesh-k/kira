# On-Call Schedule and Escalation

## Overview
Our engineering team follows a weekly on-call rotation to handle production issues. Each on-call engineer is responsible for incident response and triage during their assigned week.

## Weekly Schedule
The on-call rotation is published every Friday on the #oncall-schedule Slack channel. It runs Monday 9 AM to Sunday 11:59 PM in UTC timezone.

## During On-Call
When an alert fires:
1. Check the alert severity (P1, P2, P3) from PagerDuty
2. P1 alerts require immediate response within 5 minutes
3. P2 alerts should be responded to within 15 minutes
4. For P1 incidents, page the backup on-call engineer if you're unavailable

## Handoff Process
At end of your on-call week:
- Update the shared incident log on Notion with all issues handled
- Document root cause for any P1 incidents
- Schedule brief 30-min debrief with next week's on-call engineer
- Mark yourself as unavailable in the scheduling system for at least 1 week

## Escalation Path
If you can't resolve an issue:
- P1: Escalate to Tech Lead → Director of Engineering
- P2: Escalate to Tech Lead
- P3: Document in incident tracker, no escalation needed
