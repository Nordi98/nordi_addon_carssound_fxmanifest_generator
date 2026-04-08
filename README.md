Anleitung: FXManifest Generator
Dieses Skript scannt automatisch deine audioconfig/ und sfx/ Ordner und generiert eine fertige fxmanifest.lua für FiveM Addon Sounds.

Voraussetzungen
Windows 10 oder neuer — kein zusätzliches Programm nötig, PowerShell ist bereits vorinstalliert.

Ordnerstruktur
Deine Ressource muss so aufgebaut sein:

addon-sounds/
├── generate.bat
├── generate_manifest.ps1
├── fxmanifest.lua  ← wird automatisch erstellt
├── audioconfig/
│   ├── gb811s2_game.dat151.rel
│   ├── gb811s2_sounds.dat54.rel
│   └── ...
└── sfx/
    ├── dlc_gb811s2/
    └── ...

Schritt für Schritt
Dateien ablegen: generate.bat und generate_manifest.ps1 in den Root-Ordner deiner Ressource kopieren — also in denselben Ordner wie audioconfig/ und sfx/.
Skript starten: generate.bat doppelklicken. Ein schwarzes Fenster öffnet sich und zeigt wie viele Einträge gefunden wurden.
Ergebnis prüfen: Die fxmanifest.lua wird automatisch im selben Ordner erstellt. Sie enthält alle data_file Einträge für AUDIO_GAMEDATA, AUDIO_SOUNDDATA und AUDIO_WAVEPACK.
Neuen Sound hinzufügen: Einfach die neuen Dateien in audioconfig/ und sfx/ legen und generate.bat nochmal ausführen — das Manifest wird komplett neu generiert.

Hinweise
SFX Ordner nicht gefunden: Wenn das Skript "KEIN SFX ORDNER GEFUNDEN" ausgibt, muss der sfx/ Unterordner genauso heißen wie der audioconfig Eintrag, nur mit dem Prefix dlc_ davor. Beispiel: gb811s2 → dlc_gb811s2.

PowerShell blockiert: Falls Windows das Skript blockiert, einmal die generate.bat als Administrator ausführen.

Bestehende fxmanifest.lua: Das Skript überschreibt eine vorhandene fxmanifest.lua ohne Rückfrage. Vorher ein Backup machen falls nötig.

