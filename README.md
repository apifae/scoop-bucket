# apifae/scoop-bucket

The Scoop bucket for APIFae, a command-line tool that mocks the HTTP APIs your
code depends on and tells you when those mocks stop matching the real API.

A mock is written once, but the API it stands in for keeps changing, and tests
that use the mock go on passing against responses the API no longer sends.
APIFae serves mocks from YAML files you commit, and `apifae diff` compares each
one with the live API. It exits 1 when a mock has drifted and 2 when it can't
reach the API, so a CI job can tell drift from an outage. `apifae patch` then
writes what it found back into your mocks.

APIFae is a single native binary with no runtime to install first. The CLI is
free and will stay free.

## Install

```powershell
scoop bucket add apifae https://github.com/apifae/scoop-bucket
scoop install apifae
```

The manifest is generated on each release and installs a prebuilt binary.
Upgrade with `scoop update apifae`.

Windows binaries are not yet Authenticode-signed, so SmartScreen may warn on
first run. Verify the download against the SHA-256 in the release's
`dist-manifest.json`.

## Learn more

[Getting started](https://apifae.com/docs/getting-started) takes an OpenAPI spec
to a served mock in about a minute. The guides and the command reference are at
<https://apifae.com>. Problems: <hello@apifae.com>.

## Licence

Closed source; binaries under MIT or Apache-2.0.
