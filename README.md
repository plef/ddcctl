ddcctl: DDC monitor controls for the OSX command line
----
Adjust your external monitors' built-in controls from the OSX shell:
* brightness
* contrast

And *possibly* (if your monitor firmware is well implemented):
* input source
* built-in speaker volume
* on/off/standby
* rgb colors
* color presets
* reset

Install
----
```bash
make install
```

For an On-Screen Display using [OSDisplay.app](https://github.com/zulu-entertainment/OSDisplay):
`make CCFLAGS=-DOSD clean ddcctl`

Usage
----
Run `ddcctl -h` for some options.
[ddcctl.sh](/ddcctl.sh) is a script I use to control two PC monitors plugged into my Mac Mini.
You can point Alfred, ControlPlane, or Karabiner at it to quickly switch presets.

MacOS Shortucts
----

Pokud nechci pouzit molochy jako CotrolPane atd. ale jen klavesove zkratky,
lze zkopirovat obsah `MacOSAutomatorServices` napr. do `~/Library/Services`
a nechat je otevrit pomoci Apple `Automator.app` MacOS aplikace.

Pak staci v Nastaveni systemu - Klavesnice - Zkratky pod zalozkou Services
nastavit patricne klavesove zkratky.

Pokud ma system vice monitoru, a podari se s nimi komunikovat, v uvedenych sluzbach staci
v Automatoru nastavit sluzbe dany displej v prepinaci `-d`, a na kazdy monitor si tak udelat
kopii sluzby, pro kazdou pak vlastni klavesovou zkratku.