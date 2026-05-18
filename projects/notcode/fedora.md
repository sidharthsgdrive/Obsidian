`25/08/25` Added Resources (task manager), Blanket (ambient noises), Blur My Shell, Emoji Copy (`Ctrl + .`, edit `30/08/25` -- `Super`+`.`)
***
`26/08/25` 
Maybe the Obsidian sync issue between Fedora and Windows is due to the time mismatch thing. In an attempt to fix that, I'll follow [this guide](https://itsfoss.com/wrong-time-dual-boot/), which advises to run:
```bash
  timedatectl set-local-rtc 1
```
***
I've set the screenshot tool to `F2` for a full-screen screenshot, and `Ctrl+Shift+F2` for area selection. (edit `27/08/25`: I've changed this to `PrtScrn` to avoid conflict with renaming)
***
`27/08/25` Here's a [forum discussion](https://discussion.fedoraproject.org/t/how-to-switch-primary-gpu-for-wayland/107789/9) on how to switch the default GPU from integrated to discrete. I feel like it might benefit me to disable the integrated GPU altogether, as I don't plan on gaming on Linux in the foreseeable future anyway. This might come with its risks though; so I have to look into it further. GPU 2 seems to be struggling with running the window manager alongside Obsidian. Ahh, it might just be because I'm running off battery.
***
`29/08/25` Configured switching workspaces using `Ctrl`+`Win`+ Number keys. Also, note -- `Alt`/`Win` + `~`  switches windows of the current application.
***
`30/08/25` Installed an extension called Panel Date Format, which uses [GLib date/time format](https://docs.gtk.org/glib/method.DateTime.format.html) to format the date and time on the top panel. Currently using this format:
``` bash
dconf write /org/gnome/shell/extensions/panel-date-format/format "'%d %b | %k:%M'"
```
***
`30/08/25` Disabled this service called `ibus` which had been preventing me from setting the Emoji picker to its Windows shortcut. 
```bash
sudo mv /bin/ibus-daemon /bin/ibus-daemon.bak
```
***
`04/09/25` Set two new shortcuts:
`Ctrl+Super+Shift+S` -- power off
`Ctrl+Super+Shift+R` -- restart
***
`10/09/25` I updated Fedora yesterday, and the only problem I encountered was `ibus` turning itself back on, which I fixed with the aforementioned command.
***
`11/09/25` I found out how to disable the password requirements for certain sudo commands.
```bash
sudo visudo
```

Inside the nano interface, added these two lines:
```sudoers
user host = (root) NOPASSWD: /sbin/shutdown
user host = (root) NOPASSWD: /sbin/reboot
```

This doesn't seem to work with aliases defined in `~/.bashrc`. I'll try again some other time.
***
`14/09/25` In an attempt to fix the Chrome authentication keyring on launch issue, I acted on the advice of [this](https://askubuntu.com/questions/31786/chrome-asks-for-password-to-unlock-keyring-on-startup) StackOverflow answer, and changed the last line of the .desktop file to 
```
Exec=/usr/bin/google-chrome-stable --password-store=basic %U
```
***
`20/09/25` Encountered a weird issue where the system freezes and the Capslock blinks rapidly. From cursory searches, I think it indicates a kernel crash. This occured once seemingly at random, then again a few minutes after a reboot. This was yesterday.
Today there doesn't seem to be a problem.
***
`01/10/25` I've been facing the old network adapter issues I used to have in Windows, and sometimes Bluetooth acts up too. I considered buying [this adapter](https://www.amazon.in/Adapter-Parent-600-Mbps-Bluetooth/dp/B0FP92L1W2?th=1) for WiFi and Bluetooth that supports Linux, but there seems to be a stopgap solution:
```bash
systemctl restart NetworkManager.service
```
***
`05/10/25` Followed [this guide](https://9to5linux.com/how-to-switch-primary-gpu-to-nvidia-on-wayland-for-kde-plasma-and-gnome) to switch the default GPU to Nvidia, and it worked flawlessly.
`11/10/25` Reverted back to the integrated GPU, after facing several issues, especially with Firefox on entering fullscreen, but also frequent graphical glitching after suspend.
***
`11/10/25` Dabbled with `rfkill`. Running `rfkill` shows a list of connected devices. However, the disabling of devices is not persistent, and it seems to just act as an on-off switch for wifi or bluetooth as a whole.
***
`12/10/25` Added the Dash-To-Dock extension for a clean, MacOS style dock. Configured it to close windows on middle click.
***
`18/10/25` I searched for a solution to the consistent freeze issue, and found [this article](https://discussion.fedoraproject.org/t/consistent-screen-freezes-after-upgrading-to-f42/149113/5) on the forums which suggested setting the power profile to balanced.
***
`24/10/25` In Problem Reporting, this error seems to be the cause of system freezes. I must look into it when I have the time.
![[Pasted image 20251024071644.png]]
```
A kernel problem occurred, but your kernel has been tainted (flags:GDWO). Explanation:
D - Kernel has oopsed before.
W - Kernel issued warning.
O - Out-of-tree module has been loaded.
Kernel maintainers are unable to diagnose tainted reports. Tainted modules: nvidia_drm,nvidia_modeset,nvidia_uvm,nvidia.
```
***
`31/10/25` In order to resolve an error with downloading Cisco's openh264 packages, added these lines to `/etc/hosts`:
```
18.66.57.8 ciscobinary.openh264.org
18.66.57.97 ciscobinary.openh264.org
18.66.57.74 ciscobinary.openh264.org
18.66.57.9 ciscobinary.openh264.org
```
This was done as per the advice of [this](https://www.reddit.com/r/Fedora/comments/1mrmwen/comment/n8yz6kl/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button) reddit comment.
***
`07/11/25` Ran these commands on the advice of [this](https://unix.stackexchange.com/questions/324843/chrome-harasses-me-for-a-keychain-password-at-startup) stackexchange post, to try to resolve the Chrome keyring issue:
```bash
cp -r ~/.local/share/keyrings ~/keyrings-backup
rm ~/.local/share/keyrings/*
```
***
`13/11/25` Rebound close app to Super+Q. Got the Power Dial extension, activated with Alt+F4.
***
`18/11/25` Installed the Tiling Shell extension and configured it a bit.
***
`23/11/25` [Followed these instructions](https://copr.fedorainfracloud.org/coprs/uriesk/minecraft-wayland-glfw-git/) to try to fix the minecraft performance.
Lunar client folder location:
`/home/sidharth/.var/app/com.lunarclient.LunarClient/.lunarclient/profiles/lunar/1.21`
***
`03/12/25`  Learned that I can use `pgrep` to search for PIDs.
```bash
pgrep java -l
kill <pid>
```
***
`06/12/25` In the proces of installing a rust CLI tool `leetcode-cli`, had to run this to add the cargo binaries to my PATH:
```bash
echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc
```
https://www.perplexity.ai/search/i-get-the-following-message-wh-LcqBrnlTQ0ehZ_8mUrD4Tw
***
`30/12/25` Flush DNS cache:
```bash
sudo systemd-resolve --flush-caches
```
***
`01/01/26` Found this CLI program from a YSAP video: `bat`. It's like `cat` but with line numbers and syntax highlighting.
***
`03/01/26` Used `dconf-editor` to disable the close button.
`org.gnome.desktop.wm.preferences` -> button-layout:
`appmenu:close` => `appmenu:`
***
`28/02/26` Edited `sudoers` using `visudo` to enable `pwfeedback`, by adding the line 
```bash
Defaults pwfeedback
```
***
`07/04/26` Added the toggle top bar extension, which uses the hotkey `Ctrl+Super+T`.