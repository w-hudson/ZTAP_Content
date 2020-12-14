---
title: "Event Tiers"
weight: 1
---
Event Tiers are how CRITICAL**START** classifies the severity of events that are ingested from security products. You can use the various Orchestration features ([Playbooks](/ztap/orchestration/playbooks/), [Filters](/ztap/orchestration/filters/), and [Lists](/ztap/orchestration/lists/)) to reclassify events that should be placed in a different Tier. 

- **Tier 1** (Trigger): Tier 1 events will **always** create an Alert. If an event is classified as Tier 1 through a Filter, the event will ignore all other criteria and be logged as an Alert. 

- **Tier 2** (Observations): Tier 2 events are not necessarily malicious by themselves, but can provide additional context with other events. Observation events will not create an Alert, however, they will be appended to any Alert with Trigger events that occur on the same host within a specific time frame.

- **Tier 3** (Whitelisted): Tier 3 events are considerd "known good”. Tier 3 events have been added to the ZTAP whitelist either manually or by a Filter. Whitelisted events will not create an Alert, however, they will be appened to any Alert with Trigger events that occur on the same host within a specific time frame.

- **Tier 4** (Discard): Tier 4 events will not be appended to an Alert if they are observed again. This is useful for situations with sensitive data such as clear text passwords. Discarded events will not generate an Alert and the data in these events is intentionally not recorded for security purposes.
