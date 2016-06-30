# outofdate-notifications-system-addon
This system addon notifies users that they are out of date via a doorhanger in the browser

## Telemetry
This addon sends telemetry pings when it starts, when the doorhanger is shown,
and when the button in the doorhanger linking to the download page is clicked.

The payload of these pings is two flags indicating whether the doorhanger has
been shown and whether the button has been clicked. The default
application data included in all pings, as documented in the
[common ping format](https://gecko.readthedocs.io/en/latest/toolkit/components/telemetry/telemetry/common-ping.html),
are also present, but not the optional environment data or client ID.

These pings will not be sent if telemetry is disabled.
