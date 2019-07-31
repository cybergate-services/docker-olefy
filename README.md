# docker-olefy

This  container is used with Rspamd in OpenEMAIL. olefy is a little helper socket to use oletools with rspamd.  Please find updates and issues here: https://github.com/HeinleinSupport/olefy 

# olefy - oletools verify over TCP socket

Small Python Daemon to use oletools over TCP sockets. Mainly to use oletools in [Rspamd](https://github.com/rspamd/rspamd).

## State of Development

This Daemon is production tested but maybe not bug free. Feel free to test and
please report any issues.

## How it works

olefy expects office documents to be send to the TCP socket. Currently olefy saves
the stream into a tmp file, calls olevba3 and returns the scan result as json.

## Future plans

Debug some issues and use oletools directly in olefy and scan inline.
Also olefy should rescan with rtfobj when olevba reports a RTF file.

As the protocol is flexible we will integrate other tools and services as needed.
(Pyzor will be next)

## oletools

[github: oletools - python tools to analyze MS OLE2 files](https://github.com/decalage2/oletools)

[http://www.decalage.info/python/oletools](http://www.decalage.info/python/oletools)

oletools is a package of python tools to analyze Microsoft OLE2 files (also called Structured Storage, Compound File Binary Format or Compound Document File Format), such as Microsoft Office documents or Outlook messages, mainly for malware analysis, forensics and debugging. It is based on the olefile parser. See [http://www.decalage.info/python/oletools](http://www.decalage.info/python/oletools) for more info.
