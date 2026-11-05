# BBCMicro.Alternate update database

This repository is the [MiSTer Downloader](https://github.com/MiSTer-devel/Downloader_MiSTer) database for
**[BBCMicro.Alternate](https://github.com/Welsh71/BBCMicro.Alternate_MiSTer)**, an enhanced BBC Micro
Model B / Master 128 core for MiSTer. Add it once, and `update` / `update_all` keep the core up to date.

It installs:

- `_Computer/BBCMicro.Alternate._YYYYMMDD.rbf`: the latest release of the core
- `games/BBCMicro.Alternate/sounds.rom`: the disc drive sound samples (optional feature, off by default)

It sits alongside the official BBC Micro core (`BBCMicro_YYYYMMDD.rbf`) without replacing it or its settings.

## Adding it to your MiSTer

**Easy way:** download
[downloader_Welsh71_BBCMicro.Alternate_DB.zip](https://raw.githubusercontent.com/Welsh71/BBCMicro.Alternate_DB/db/downloader_Welsh71_BBCMicro.Alternate_DB.zip),
extract the `.ini` file from it and copy it to the root of the SD card, next to `downloader.ini`.

**Or by hand:** add these lines to the end of `downloader.ini` on the SD card:

```ini
[Welsh71/BBCMicro.Alternate_DB]
db_url = https://raw.githubusercontent.com/Welsh71/BBCMicro.Alternate_DB/db/db.json.zip
```

Then run `update` or `update_all` as usual.

## For the maintainer

Everything outside `README.md`, `LICENSE`, `.github/` and `external_files.csv` is mirrored 1:1 onto users'
SD cards. At each release, replace the `.rbf` in `_Computer/` with the new
`BBCMicro.Alternate._YYYYMMDD.rbf` (the same file as in the source repo's `releases/` folder) and push;
the GitHub Action rebuilds `db.json.zip` on the `db` branch. Built from theypsilon's
[DB-Template_MiSTer](https://github.com/theypsilon/DB-Template_MiSTer).
