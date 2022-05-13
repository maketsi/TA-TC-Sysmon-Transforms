# TA-TC-Sysmon-Transforms

This is a supplemental package for TA-TC-Sysmon, providing index-time transforms that aid in large-scale deployments:
* provide massive search-time performance improvements via event-specific sourcetypes
* pack the data by throwing away unnecessary header information, reducing disk and license costs by 30..60%.

This addon should be placed on heavy forwarders or indexers, whichever receive and parse the traffic first from universal forwarders.

The parent supplementary package TA-TC-Sysmon (not included) contains search-time knowledge objects, and is meant to be placed in search heads.

Original inbound events are expected to have sourcetype XmlWinEventLog:Microsoft-Windows-Sysmon/Operational
and are transformed to use sourcetypes 'sysmon:events:$name' where $name describes the event type ID in text (e.g. 'sysmon:events:processcreated').
Additionally, event type ID (e.g. 1) is extracted to CIM-compatible index-time field 'signature_id'.


## Sysmon support

This addon is up-to-date with Sysmon 13.34, supporting all its event types. Further upgrades to bundled CSV lookup file
are needed if new event IDs are introduced. Unknown event IDs will default to sourcetype 'sysmon:events' and are still parseable
by TA-TC-Sysmon, but that should be considered a fallback.


## Requirements

This addon uses INGEST_EVAL transform with lookup() function for sourcetype mapping and as such requires Splunk version 8.1.0 or higher.


## Author

Markku Parviainen, 2019-2022
