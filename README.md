![Fuxion logo](https://github.com/FluxionNetwork/fluxion-app/raw/master/logos/logo.jpg)

# Fluxion is the future of MITM WPA attacks
Fluxion is a security auditing and social-engineering research tool. It is a remake of linset by vk496 with (hopefully) less bugs and more functionality. The script attempts to retrieve the WPA/WPA2 key from a target access point by means of a social engineering (phising) attack. It's compatible with the latest release of Kali (rolling). Fluxion's attacks' setup is mostly manual, but experimental auto-mode handles some of the attacks' setup parameters. Read the [FAQ](https://github.com/FluxionNetwork/fluxion/wiki/FAQ) before requesting issues.
Currently the fake ap does not work. Until now this is a wip project.

If you need quick help, fluxion is also avaible on gitter. You can talk with us [here](https://gitter.im/FluxionNetwork/Lobby)
## Installation
Read [this](https://github.com/FluxionNetwork/fluxion/wiki/Generate-ssh-keys) before you follow the following steps.
<br>
**Download the latest revision**
```
git clone --recursive git@github.com:FluxionNetwork/fluxion-app.git 
```
**Switch to tool's directory**
```
cd fluxion-app
```
**Build the app using android studio.

## :scroll: Changelog
Fluxion gets weekly updates with new features, improvements, and bugfixes.
Be sure to check out the [changelog](https://github.com/FluxionNetwork/fluxion-app/commits/master).

## :octocat: How to contribute
All contributions are welcome! Code, documentation, graphics, and design suggestions are welcome; use GitHub to its fullest. Submit pull requests, contribute tutorials or other wiki content -- whatever you have to offer, it'll be appreciated but please follow the [style guide](https://github.com/FluxionNetwork/fluxion/wiki/Code-style-guide).

## :book: How it works
* Scan for a target wireless network.
* Launch the `Handshake Snooper` attack.
* Capture a handshake (necessary for password verification).
* Launch `Captive Portal` attack.
* Spawns a rogue (fake) AP, imitating the original access point.
* Spawns a DNS server, redirecting all requests to the attacker's host running the captive portal.
* Spawns a web server, serving the captive portal which prompts users for their WPA/WPA2 key.
* Spawns a jammer, deauthenticating all clients from original AP and luring them to the rogue AP.
* All authentication attempts at the captive portal are checked against the handshake file captured earlier.
* The attack will automatically terminate once a correct key has been submitted.
* The key will be logged and clients will be allowed to reconnect to the target access point.


## :heavy_exclamation_mark: Requirements

Simple build the app using the android studio. Some code is obsolete anf get fixed as soon as possible.

## Related work

For development I use vim and tmux. Here are my [dotfiles](https://github.com/deltaxflux/takumi/)
## :octocat: Credits
1. l3op - contributor
2. dlinkproto - contributor
3. vk496 - developer of linset
4. Derv82 - @Wifite/2
5. Princeofguilty - @webpages and @buteforce
6. Photos for wiki @http://www.kalitutorials.net
7. Ons Ali @wallpaper
8. PappleTec @sites
9. MPX4132 - Fluxion V3

## Disclaimer
* Authors do not own the logos under the `/attacks/Captive Portal/sites/` directory. Copyright Disclaimer Under Section 107 of the Copyright Act 1976, allowance is made for "fair use" for purposes such as criticism, comment, news reporting, teaching, scholarship, and research.

* The usage of Fluxion to attack infrastructure without prior mutual consent could be considered an illegal activity, and is highly discouraged by its authors and developers. It is the end users responsibility to obey all applicable local, state and federal laws. Authors assume no liability and are not responsible for any misuse or damage caused by this program.

## Note
* :heavy_exclamation_mark: Beware of sites pretending to be related with the Fluxion Project. These may be delivering malware.

* Fluxion **DOES NOT WORK** on Linux Subsystem For Windows 10, because the subsystem doesn't allow access to network interfaces. Any Issue regarding the same would be **Closed Immediately**


