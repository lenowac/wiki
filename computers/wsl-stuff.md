# WSL Workarounds

## Auto-Startup

1. win+r, go to `%AppData%\Microsoft\Windows\Start Menu\Programs\Startup`
2. create the file wsl-start.vbe and add this:

```vbs
Set ws = CreateObject("Wscript.Shell")
ws.run "wsl -d ubuntu -u root /etc/init.wsl start", vbhide
```

3. create the referenced file and do something there. Mine contains:

```sh
#! /bin/sh
/etc/init.d/ssh $1
```

<br/>

## Mount external Storage

[Original Article](https://www.scivision.dev/mount-usb-drives-windows-subsystem-for-linux/)
replace "f" with the respective drive letter:

```sh
mkdir /mnt/f

mount -t drvfs f: /mnt/f
```
