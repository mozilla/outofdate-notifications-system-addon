# outofdate-notifications-system-addon
This system addon notifies users that they are out of date via a doorhanger in the browser

## Telemetry
This addon sends telemetry pings when it starts, when the doorhanger is shown,
and when the button in the doorhanger linking to the download page is clicked.

The structure of these pings is a JSON object fitting the [common ping format](https://gecko.readthedocs.io/en/latest/toolkit/components/telemetry/telemetry/common-ping.html)
with the ping type set to "outofdate-notifications-system-addon" and payload
data in this form:

    {
      shown: <bool>,
      clicked: <bool>
    }

The two flags indicate whether the doorhanger notification has been shown, and
whether the button linking to the download page has been clicked.
The optional environment data from the common ping format is not included,
but the optional client ID is included, so that these pings can be correlated
with other telemetry.

These pings will not be sent if telemetry is disabled.

## Build, Test & Release
Refer to https://wiki.mozilla.org/Firefox/Go_Faster/Releasing_an_add-on_mechanics for the latest instructions.
