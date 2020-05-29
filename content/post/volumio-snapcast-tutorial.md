---
title: "Install volumio with snapcast support"
date: 2020-05-30T01:16:27+02:00
---

In this tutorial, you will see my configuration to let volumio work with snapcast without any headaches.

I am running volumio on a raspberry pi 4 with 4 gb ram. The snapcast clients are raspberry pi 3 B+. Both with raspbian (latest version). Snapcast client follows the instructions on https://github.com/badaix/snapcast#debian. Volumio follows the instructions on https://volumio.org/get-started/.

After the installation of volumio, i installed via volumio UI the following addon: spotify-connect2.
Now enable the dev ssh connection (https://volumio.github.io/docs/User_Manual/SSH.html) and login via putty or ssh. You should clone the following repo https://github.com/Saiyato/volumio-plugin-helper and cd into it. Now you can install the current version of volumio snapcast plugin with the following command:

```bash
sh volumio_install_from_zip.sh Saiyato volumio-snapcast-plugin
```

Now you should everything configure like me and after this, restart your volumio installation with
```bash
sudo systemctl restart volumio
```

You can found the following config files in folder '/etc'.

## MPD.conf
```bash

```

## spop.conf
```bash

```

## asound.conf
```bash

```
