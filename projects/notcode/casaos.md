[EASY Budget Minecraft Servers with Crafty](https://www.youtube.com/watch?v=bAGTwBURBXc)
[$75 Dedicated Minecraft Server Budget Build 2025 No Port Forwarding Casa OS and Crafty Controller!](https://youtu.be/uZgY6--IOgM?si=rTe3_BpyQqZeXdET)
***
`21/11/25` Tried installing Debian, but ran into issues with Network configuration. I tried to configure manually, but couldn't log into the BSNL wifi's portal.
Tomorrow I'll try with Ubuntu server instead.
***
`24/11/25` When installing Ubuntu server, the ethernet doesn't seem to be up. I'll proceed with WiFi for now. 
LMAO. turns out I was plugging the ethernet cable in upside down the whole time.

Decided to go with Debian after all.
hostname: `mc-server`
domain name: `local`
username: `sidharth`
password: `sidharth`

Installed CasaOS, with password saved to Bitwarden.
https://github.com/IceWhaleTech/CasaOS/issues/2387

Crafty: 
- username: `admin`
- password location: ``app/config/default-creds.txt``
- changed to: `WiseMystic@42`
![[Pasted image 20251129160424.png]]



***
curl -SsL https://playit-cloud.github.io/ppa/key.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/playit.gpg >/dev/null
echo "deb [signed-by=/etc/apt/trusted.gpg.d/playit.gpg] https://playit-cloud.github.io/ppa/data ./" | sudo tee /etc/apt/sources.list.d/playit-cloud.list
sudo apt update
sudo apt install playit

***
https://www.perplexity.ai/search/debian-server-prevent-from-goi-_0w3ypfdTTePYQs779Qyqg#0
in `/etc/systemd/logind.conf`,
Uncommented these lines, and changed "suspend" to "ignore": 
```conf
HandleLidSwitch=ignore
HandleLidSwitchExternalPower=ignore
HandleLidSwitchDocked=ignore

```

***
Crafty
user: `admin`
pass: `sidharth`
***
`03/12/25` Used 
```bash
sudo dpkg-reconfigure tzdata
```
to fix time zone issues in Crafty.
***
https://modrinth.com/mod/noend
***
`13/12/25` Mods I haven't reinstalled after the update:
- C2ME: requires a newer JDK, can't bother with that rn
- Krypton: hasn't released
- Clumps: hasn't released
- Chunky: felt it wasn't necessary
- **SkinRestorer: hasn't released**
- https://modrinth.com/mod/modernfix: didn't install before either, should install