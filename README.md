# Job Assistant releases

Updates for the team's Job Assistant apps (team internal).

- **Windows:** `Job-Assistant-Setup-<version>.exe`, described by `latest.json`
- **Android:** `Job-Assistant-<version>.apk`, described by `latest-android.json`

Every copy of the apps reads the two `latest` files of the newest release, from
`https://github.com/web3presale-cyber/job-assistant-releases/releases/latest/download/`, when it starts and every
30 minutes. A newer version shows a red bar with an Update button. The apps check each download against the size
and SHA-256 sum in these files before installing it.

New versions are published by the workflow in `.github/workflows/publish.yml`: the release script pushes the files
to the branch `incoming`; the workflow checks them, publishes the release and deletes the branch.
