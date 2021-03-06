# Presage based input predictor for the Sailfish OS
This input handler plugin provides an alternative text prediction solution to the Xt9 engine shipped by the Jolla. It could be useful if you are using community supported language pack or if you have a ported device.

## Features ##
The predicted words are generated by the presage library. The presage predictions coming from various plugins:
* ngram: this plugin uses a database generated from text corpuses. Basically it tries to match your typed word with sentence fragments in the database and offers the words from those segments. 
* user-ngram: this plugin works the same manner as the ngram, but it's database is expanded continously as you type. 
* hunspell: it tries to spellcheck the currently typed word with hunspell and if it found to be mistyped it will suggest the correct version as well

# Distribution, releases
The released build of this plugin (and keyboard layouts utilizing it) can be downloaded from the openrepos:
https://openrepos.net/content/sailfishkeyboard/keyboard-presage-enus

https://openrepos.net/content/sailfishkeyboard/keyboard-presage-etee

https://openrepos.net/content/sailfishkeyboard/maliit-plugin-presage

# Debugging (khm. troubleshooting) info
To debug a keyboard plugin you should run on your device:
```
pkill maliit-server; MALIIT_DEBUG=enabled maliit-server
```
(Console output is controlled by the MALIIT_DEBUG variable)
If you know how to hook this through the GDB in the SailfishOS SDK let me know.

# Thanks, inspiration, links
Matteo Vescovi who developed the Presage:
http://presage.sourceforge.net/

Hanhsuan's predictor helped me at the beginnging a lot
https://github.com/hanhsuan/jolla-chewing

Pekka Vuorela for the debugging tips
