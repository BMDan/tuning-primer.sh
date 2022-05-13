# Security Policy

## Supported Versions

Only the latest version (i.e.,
[`main`](https://github.com/BMDan/tuning-primer.sh/)) is supported.

All other versions (in particular, the version hosted on Day32) are not and
**cannot be** supported.

## Reporting a Vulnerability

Please report all vulnerabilities directly to Dan Reif.  If you are unable
to locate his contact information, open an issue to request it.  For truly
urgent issues, you may use multiple means of contact to ensure the message
is received as quickly as possible.

I will endeavor to acknowledge any reported vulnerability within 72 hours
of receipt.

## Vulnerability Definition

Please be aware that this script is intended to be run by administrators,
who already generally already have privileged access to the machines on
which the script is running.  Therefore, an example vulnerability that
uses an unusual set of characters in a password (see #20) to make the
script not run or to return bizarre results is not considered a meaningful
vulnerability, since the administrator presumably wouldn't use such a
password in the first place.

Conversely, however, an example vulnerability that allowed someone with
`Create_priv` to create a schema with a special name that triggers arbitrary
code execution in the context of the user running this script when the script
is invoked is clearly a vulnerability, and will be addressed with the utmost
urgency.
