# DDB Game Log – server endpoints

The DDB Game Log Foundry module reads this file at connect time to find the current
relay server, so the servers can move without releasing a new module version.

Published on purpose: the endpoint is inside every module build anyway. The module only
accepts `wss://` URLs whose host is on an allowlist compiled into the release, so this
file cannot redirect anyone to an unknown server.
