Emby Mediaserver - Simple Network Attached Media Storage
========================================================

`Emby`_ is an easy to use media server that allows you to bring all 
of your home videos, music, and photos together into one place. The 
TurnKey Emby Mediaserver combines Windows-compatible network file 
sharing with web based library and file managers. Emby can 
automatically convert and stream your media on-the-fly to play on 
any DLNA supported device. Additionally TurnKey Emby Mediaserver
includes support for SMB (via `Samba`_), SFTP, NFS, WebDAV (via 
`SambaDAV`_) and rsync file transfer protocols. The server is 
configured to allow users to manage files in private or public 
storage. 

This appliance includes all the standard features in `TurnKey Core`_,
and on top of that:

- SSL support out of the box.
- `Emby`_ providing WebUI on ports 8096 and 8920 (https).
- Webmin module for configuring Samba.
- Includes popular compression support (zip, rar, bz2).
- Includes flip to convert text file endings between UNIX and DOS
  formats.
- `SambaDAV`_ providing WebUI and WebDAV access.
- Media server (`Emby`_) configurations:
   
   - Preconfigured Music, Movies, TVShows, and Photos directories
   - Preconfigured path substitution for samba access

- File server (`Samba`_) configurations:
   
   - Preconfigured wordgroup: WORKGROUP
   - Preconfigured netbios name: MEDIASERVER
   - Configured Samba and UNIX users/groups synchronization (CLI and
     Webmin).
   - Configured root as administrative samba user.
   - Configured shares:
      
      - Users home directory.
      - Public storage.
      - CD-ROM with automount and umount hooks (/media/cdrom).

- Access your files securely from anywhere via `SambaDAV`_:
   
   - web GUI access to your files, with online previews of major formats and drag-n-drop
     support.
   - Pre-configured authentication (Samba).
   - Pre-configured repositories (storage, user home directories).

- Default storage: */srv/storage*
- Accessing file server via samba on the command line::

    smbclient //1.0.0.61/storage -Uroot
    mount -t cifs //1.0.0.61/storage /mnt -o username=root,password=PASSWORD

Credentials *(passwords set at first boot)*
-------------------------------------------

-  Emby: username **emby**
-  Webmin, Webshell, SSH, Samba: username **root**
-  Web based file manager (SambaDAV):
   
   - username **root** (or Samba users)

.. _Emby: https://emby.media/
.. _TurnKey Core: https://www.turnkeylinux.org/core
.. _Samba: http://www.samba.org/samba/what_is_samba.html
.. _SambaDAV: https://github.com/1afa/sambadav

