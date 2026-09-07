# apifae/scoop-bucket

Scoop bucket for the [APIFae](https://apifae.com) CLI.

```powershell
scoop bucket add apifae https://github.com/apifae/scoop-bucket
scoop install apifae
```

The manifest is generated on each release and installs a prebuilt binary. The
CLI's source is not public.

Windows binaries are not yet Authenticode-signed, so SmartScreen may warn on
first run. Verify the download against the SHA-256 in the release's
`dist-manifest.json`.

Upgrade with `scoop update apifae`. Problems: <team@apifae.com>.
