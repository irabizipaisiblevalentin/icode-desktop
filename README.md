# iCode Desktop

iCode is the AI coding agent as a desktop app. It works exactly like the terminal
workflow — same engine, same sessions, same models — with a native window, a project
picker, and a 21-day trial that gates itself on your machine.

The installers on this repo's [latest release](../../releases/latest) are the same
builds published on the [iCode website](https://icode-website-sand.vercel.app).

## Install

- **Windows**: run `iCode-Setup-<version>-<arch>.exe` (x64 or arm64).
- **macOS**: open `iCode-<version>-<arch>.dmg` and drag iCode to Applications (Apple
  Silicon or Intel). Unsigned: right-click the app → Open the first time.
- **Linux / ChromeOS**: install `icode_<version>_<arch>.deb` with your package manager,
  or run the AppImage (`chmod +x` first), or unpack the `tar.gz`.

## License

Every install runs a 21-day trial. After that, a passcode is required. Paid licenses
automatically fall back to the OpenRouter free models router (owned by the iCode
project) when Big Pickle hits its limit — no OpenRouter API key is ever needed from
you. Trial users stay on Big Pickle and the other free models.

## Security note

The installers embed the project owner's OpenRouter API key as the paid fallback
router key. The key is readable by anyone who extracts the installer, so treat it as
public. To rotate it, build a new release with a fresh key in
`resources/fallback-key.txt` (gitignored) and re-publish.

This repository ships release binaries only. Source is not published here.
