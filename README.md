# SRVB OS Noctalia

<p align="center">
  Ein persönliches Vanilla-OS-Image mit dem Ziel eines Wayland-Desktops aus Noctalia und Umbriel.
</p>

## Überblick

SRVB OS Noctalia ist eine persönliche Distribution-Konfiguration auf Basis von
Vanilla OS Core. Als Desktop sind Noctalia als Shell und Umbriel als
Wayland-Compositor vorgesehen, ohne den GNOME-Desktop des offiziellen
Vanilla-OS-Desktop-Images zu übernehmen.

Das Projekt befindet sich im Aufbau. Das aktuelle Image enthält bislang die
Core-Basis und erste Ergänzungen, noch keinen fertig eingerichteten Desktop.
Es ist keine Variante des Fedora-bootc-basierten
[SRVB OS](https://github.com/SRVB/srvb-os), sondern verwendet Vanilla OS und ABRoot.

## Enthalten

- Vanilla OS Core als Systembasis
- ABRoot für image-basierte Systemaktualisierungen und Rollbacks
- ABRoot-Konfiguration mit Verweis auf das eigene SRVB-OS-Noctalia-Image
- Vanilla Tools: `lpkg` zum Sperren und Entsperren der APT-/dpkg-Werkzeuge und
  `cur-gpu` zur Ermittlung der verwendeten GPU und des Treibers
- Vim als Terminal-Texteditor

## Geplanter Desktop

- Noctalia als Desktop-Shell
- Umbriel als Wayland-Compositor
- Die für den Desktop benötigte Sitzungs-, Portal- und Systemintegration

Diese Komponenten sind im aktuellen Rezept noch nicht eingebunden.
`lpkg` ist bereits enthalten; eine abschließende Sperre der Paketwerkzeuge
ist derzeit noch nicht eingerichtet.

## Image

Das Image für den Hauptbranch wird unter folgender Adresse veröffentlicht:

```text
ghcr.io/srvb/srvb-os-noctalia:main
```

## Hinweis zur Verwendung

SRVB OS Noctalia ist eine persönliche Konfiguration in Entwicklung und erhebt
nicht den Anspruch, eine allgemeingültige Desktop-Distribution zu sein.
Das Image ist derzeit nicht als vollständiger Desktop für den produktiven
Einsatz vorgesehen.

Die Verwendung erfolgt auf eigene Gefahr. Vor einem Systemwechsel sollte ein
Backup wichtiger Daten vorhanden sein. Dieses Image verwendet ABRoot und ist
nicht für einen Wechsel mit `bootc switch` vorgesehen.

## Lizenz

Der Lizenztext dieses Projekts befindet sich in [LICENSE.txt](LICENSE.txt)
(GNU General Public License, Version 3).

Die im Image enthaltenen Komponenten und Pakete stammen von Drittanbietern und
unterliegen ihren jeweiligen Lizenzen. Für diese gelten die Lizenz- und
Urheberrechtshinweise der jeweiligen Projekte und Pakete.
