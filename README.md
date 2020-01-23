# TA-TC-Sysmon-Transforms

This is a supplemental package for TA-TC-Sysmon, providing index-time transforms. This should be placed on heavy forwarders or indexers,
which ever receives the traffic first.

The parent package TA-TC-Sysmon contains the search-time knowledge objects, and is meant to be placed in search heads.

Original events are expected to have sourcetype XmlWinEventLog:Microsoft-Windows-Sysmon/Operational


## Author

Markku Parviainen, 2019
