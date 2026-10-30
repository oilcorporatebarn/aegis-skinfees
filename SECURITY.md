# Security Policy

## Supported versions

| Version | Status |
| --- | --- |
| 0.9 beta | Full support while the beta runs |
| earlier internal builds | Replace before reporting |

The beta line moves fast. A report against a build older than the last tag is
usually answered with "update first" — the fix may already be in.

## Reporting

Use the private vulnerability reporting form. Public issues are fine for
anything that cannot be abused, including calculation bugs that only lose
precision.

A report should carry:

- The build number from the About panel
- Venue pair and currencies involved
- Expected number, observed number, and the fee assumptions in effect

## Engine-specific rules

- Fee math is deterministic and runs on device. Two machines with the same
  assumptions must produce the same number; if they do not, that is a
  security-grade bug.
- FX conversion uses a fixed table refreshed per release. A report that
  hinges on live rates is a feature discussion, not an advisory.
- The demo fixture is read-only. Crashes that require editing the fixture are
  still accepted, with a note on how you edited it.

## Disclosure

Fixed advisories ship with the release. Each one states the affected
versions, the code path, and the minimal fix — enough for fork maintainers to
verify their own trees without a second report.

## Credits

Reporters are named in the release notes unless they ask to stay anonymous.
Repeated quality reports earn a line in CONTRIBUTORS.md, if wanted.
