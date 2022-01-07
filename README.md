# ProtonDB info for SteamGifts

Usercript for SteamGifts.

Adds Linux compatibility info from ProtonDB to games in giveaways on SteamGifts (near comments and entries counters on the home page and above remaining time on the giveaway page).

Show overall game tier (*Linux compatibility/playability state of the game*) for each giveaway. In the tooltip (*shown on mouseover*) it also shows the recent tier based on recent reports (*with new Proton versions*) and the count of reports for the game.

To reduce the count of requests to the Steam and ProtonDB servers (and prevent blocking/blacklisting on those servers) script limits requests to 3 per second and caches results in Tampermonkey storage. After caching games info script will automatically update the cache after 1 week (*on demand when game will be on giveaway, so it can be more than week*) to have actual info.

### Steamgifts pages processed by script:
* Home page
* Giveaway page
* Entered giveaways list

## Compatibility:
* \[+\] Compatible with **ESGST** addon (*normal view only*).
* \[+\] Compatible with **Dark Reader** addon.
* Should be compatible with another "Dark-styling" addons, but may have visual issues.


* \[-\] Does not work with grid-view of **ESGST** addon (*ESGST option 3.27*).
* \[-\] Does not work with endless scrolling of **ESGST** addon (*ESGST option 2.8*).
* \[-\] Does not work with giveaways extractor of **ESGST** addon (*ESGST option 3.17*).

## Known issues:
* **ESGST** can move ProtonDB info block to the begin of line with commets and entries counters on some or all giveaways on Steamgifts homepage.
* For packages script show ProtonDB info only for the game with lowest Steam appid: if package contains game+dlc - usual game have lower appid than dlcs, but if package contains multiple games - script will show info only for one game (*with lowest appid*).

## Preview
* SteamGifts homepage in **Firefox** on **Xubuntu Linux** without another addons:

![Preview](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/img/linux-firefox.jpg)

* SteamGifts homepage in **Firefox** on **Xubuntu Linux** with **"ESGST"** and **"Dark Reader"** addons:

![Preview](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/img/linux-firefox-esgst-darkreader.jpg)

* Giveaway page in **Firefox** on **Xubuntu Linux** with **"ESGST"** and **"Dark Reader"** addons:

![Preview](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/img/linux-firefox-esgst-darkreader--single.png)

* Entered giveaways list in **Firefox** on **Xubuntu Linux** with **"ESGST"** and **"Dark Reader"** addons:

![Preview](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/img/linux-firefox-esgst-darkreader--entered.jpg)

* SteamGifts homepage in **Vivaldi** (*Chromium based*) on **Windows 10** without another addons:

![Preview](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/img/win10-vivaldi.jpg)

* SteamGifts homepage in **Vivaldi** (*Chromium based*) on **Windows 10** with **"Dark Reader"** addons:

![Preview](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/img/win10-vivaldi-darkreader.jpg)

## Installation:
1. Install **"Tampermonkey"** addon for your browser:
    * **Google Chrome**: [install](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
    * **Mozilla Firefox**: [install](https://addons.mozilla.org/ru/firefox/addon/tampermonkey/)
    * **Opera**: [install](https://addons.opera.com/en/extensions/details/tampermonkey-beta/)
    * **Safari** (MacOS): [install](https://apps.apple.com/us/app/tampermonkey/id1482490089)
    * **IE/Edge**: *not supported*
2. Install userscript: [install](https://raw.githubusercontent.com/Xeloses/sg-protondb-info/master/sg-protondb-info.user.js)

## Version history:
* 1.0.0
    * Initial release.
* 1.0.0.1
    * Add cache expiration time (default: 1 week).
