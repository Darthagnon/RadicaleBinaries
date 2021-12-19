# RadicaleBinaries
Windows binaries and build process for Radicale CalDAV/CardDAV server.

Radicale is the only easy-to-use local CalDAV/CardDAV (Calendars and Contacts) server that exists. All others require heavy lifting, horridly complicated setup or dependence on Big Tech. I'm working on a project to make it easier to use, compiling it into a single binary.

## Compile

## Sources
- Radicale [for Win10](https://radicale.org/v3.html) / [for Win7](https://radicale.org/v2.html)
- InfCloud Web Interface for Radicale ([Homepage](https://www.inf-it.com/open-source/clients/infcloud/), [GitHub](https://github.com/Unrud/RadicaleInfCloud))
- [Tutorial for how to use Radicale with iOS](https://jeffhoadley.com/2020/10/26/radicale-server-in-windows/) ([Archive.today](https://archive.ph/Bud5Q), [Archive.org](https://web.archive.org/web/20210816093906/https://jeffhoadley.com/2020/10/26/radicale-server-in-windows/))
- Workaround for iOS bugs/ports - requires port 443??? what was that website?
- [Reddit help thread 1](https://old.reddit.com/r/selfhosted/comments/p5cr14/radicale_contacts_requires_ssl_handshake_fails/) ([Archive.org](https://web.archive.org/web/20211219150220/https://old.reddit.com/r/selfhosted/comments/p5cr14/radicale_contacts_requires_ssl_handshake_fails/))

## Roadmap
1. Fully document build process (build with [nuitka](https://www.nuitka.net/pages/download.html#windows)? or [cx_freeze](https://cx-freeze.readthedocs.io/en/latest/)? or [pyinstaller](https://www.pyinstaller.org/)?)
2. Document usage with Windows, localhost web, LAN web, [Em Client](https://www.emclient.com/release-history?os=win), [Thunderbird](https://www.thunderbird.net/en-US/), [Thunderbird: Cardbook](https://addons.thunderbird.net/en-GB/thunderbird/addon/cardbook/), [Android: DavX5](https://www.davx5.com/download) ([F-Droid](https://f-droid.org/en/packages/at.bitfire.davdroid/)), iOS Calendars/Contacts
