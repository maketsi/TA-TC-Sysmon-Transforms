# TA-TC-Sysmon-Transforms

This is a supplemental package for TA-TC-Sysmon, providing index-time transforms. This should be placed on heavy forwarders or indexers,
which ever receives the traffic first.

The parent package TA-TC-Sysmon contains the search-time knowledge objects, and is meant to be placed in search heads.

Original events are expected to have sourcetype XmlWinEventLog:Microsoft-Windows-Sysmon/Operational


## Sysmon support

This addon is up-to-date with Sysmon 11.0, supporting all its event types. Further upgrades are needed if new event IDs are introduced.
Unknown event IDs will default to sane sourcetype.


## Author

Markku Parviainen, 2019-2020
