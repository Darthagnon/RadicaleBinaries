# RadicaleBinaries
Windows binaries and build process for Radicale CalDAV/CardDAV server.

Radicale is the only easy-to-use local CalDAV/CardDAV (Calendars and Contacts) server that exists. All others require heavy lifting, horridly complicated setup or dependence on Big Tech. I'm working on a project to make it easier to use, compiling it into a single binary.

## Compile

1. Install Python [v3.9.9](https://www.python.org/downloads/release/python-399/), making sure to add it to PATH
2. Make a Python virtual environment `python3 -m venv Radicale-v2.1.12` or `Radicale-v3.1.0` ("Radicale" will be used henceforth)
3. Activate the virtual environment 
4. Install Radicale of the appropriate version via
5. Install recommended dependencies
6. (or just use the provided [requirements.txt]() to download and install everything in one go
7. 

## Sources
- Radicale [v3.1.0 for Win10](https://radicale.org/v3.html) / [v2.1.12 for Win7](https://radicale.org/v2.html)
- InfCloud Web Interface for Radicale ([Homepage](https://www.inf-it.com/open-source/clients/infcloud/), [GitHub](https://github.com/Unrud/RadicaleInfCloud))
- [Tutorial for how to use Radicale with iOS](https://jeffhoadley.com/2020/10/26/radicale-server-in-windows/) ([Archive.today](https://archive.ph/Bud5Q), [Archive.org](https://web.archive.org/web/20210816093906/https://jeffhoadley.com/2020/10/26/radicale-server-in-windows/))
- [Workaround for iOS bug - iOS requires CalDAV/CardDAV servers to run on port 443 or 80](http://www.carddavserver.com/connecting/ios/) ([Archive.org](https://web.archive.org/web/20170427045958/http://www.carddavserver.com/connecting/ios/), [Archive.today](https://archive.ph/CQ158))
- [Reddit help thread 1](https://old.reddit.com/r/selfhosted/comments/p5cr14/radicale_contacts_requires_ssl_handshake_fails/) ([Archive.org](https://web.archive.org/web/20211219150220/https://old.reddit.com/r/selfhosted/comments/p5cr14/radicale_contacts_requires_ssl_handshake_fails/))
- [Reddit help thread 2](https://www.reddit.com/r/learnpython/comments/qwr6tz/can_anyone_help_me_compile_radicale/)

## Roadmap
Not necessarily in order
1. Fully document build process (build with [nuitka](https://www.nuitka.net/pages/download.html#windows)? or [cx_freeze](https://cx-freeze.readthedocs.io/en/latest/)? or [pyinstaller](https://www.pyinstaller.org/)?)
2. Document usage with:
	- Windows:
		- localhost web 
		- LAN web
		- [Em Client](https://www.emclient.com/release-history?os=win)
		- [Thunderbird](https://www.thunderbird.net/en-US/)
		- [Thunderbird: Cardbook](https://addons.thunderbird.net/en-GB/thunderbird/addon/cardbook/)
		- [Win10 Contacts PIM](https://www.ctrl.blog/entry/how-to-win10-webdav-syncengine.html) (see also [here](https://www.ctrl.blog/entry/windows-pim-sync-partnersonly.html)) 
	- Android: 
		- [DavX5](https://www.davx5.com/download) ([F-Droid](https://f-droid.org/en/packages/at.bitfire.davdroid/))
		- [DecSync CC](https://f-droid.org/packages/org.decsync.cc/)
		- [Open Contacts](https://f-droid.org/en/packages/opencontacts.open.com.opencontacts/)
		- Simple Contacts Pro ([Google Play](https://play.google.com/store/apps/details?id=com.simplemobiletools.contacts.pro), [F-Droid](https://f-droid.org/en/packages/com.simplemobiletools.contacts.pro/) - recommended to get it from [Mobilism](https://forum.mobilism.org/index.php) due to alleged cut content from free F-Droid version) 
	- iOS Calendars/Contacts (legacy iOS 7.1.2)
	- LAN/localhost VM Mac OS X Contacts/Calendars
3. Solve [related issue #891 on Radicale GitHub](https://github.com/Kozea/Radicale/issues/891)
4. Supply venv with all dependencies at least until binary builds are possible.
5. Supply binaries targeting a minimum of Win7 (which should be forwards compatible).
6. Ascertain which Python version is best. PyInstaller and some other notable projects used a maximum of Python 3.7, but now those projects are dead(ish) and PyInstaller supports Python 3.9
7. Document [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) self-signed cert process, due to complexity (and requirement for HTTPS CalDAV/CardDAV on iOS)
8. Possibly document usage with reverse proxies? e.g. [nginx](https://nginx.org/en/download.html) ([Apache](https://httpd.apache.org/download.cgi) is old and clunky, [Caddy](https://caddyserver.com/) has terrible documentation and inconsistent syntax)