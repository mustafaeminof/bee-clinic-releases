# BEE CLINIC — releases

Windows installers for **BEE CLINIC**, the dental clinic management and POS
system by [BEE Solutions IQ](https://github.com/mustafaeminof).

This repository holds no source code. It exists so a clinic — and the station's
own updater — can fetch a build without signing in to anything.

## Download

**[→ Latest release](../../releases/latest)**

| File | What it is |
|---|---|
| `BeeClinic-Setup-<version>.exe` | The installer. This is the one you want. |
| `BeeClinic-Windows-<version>.zip` | The same build with no installer, for a machine where the setup will not run. Unpack it over the install folder. |

Run the installer and answer **Yes** to the Windows permission prompt (UAC).
It installs into `C:\Program Files\BEE CLINIC`, puts a shortcut on the desktop,
and opens the port the clinic's tablets and waiting-room screens connect to.

It does **not** touch the clinic's data. The database, the backups, the patient
attachments and the exports all live under the Windows *Documents* folder, and
an install, an update and even an uninstall leave every one of them alone.

## Updating

The station checks for a new build by itself and says so on its own launcher.
Press **Download the update** and it takes a fresh backup first, downloads the
installer, and — after one permission prompt — replaces itself and starts again.
Nothing to type, and nobody has to visit the clinic.

`latest.json` beside this file is the manifest the station reads. It is written
by CI on every release and is one of four independent routes the updater tries,
so a clinic whose connection cannot reach the GitHub API still sees new builds.

## Support

The station's own **Settings → About** carries the number to call, along with
the build, the schema and the station id a support call will ask for.
