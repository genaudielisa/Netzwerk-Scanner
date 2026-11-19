# Netzwerk-Scanner 🌐

Ein kleines Python-Programm, das alle Adressen eines Netzwerks anpingt und die erreichbaren Geräte auflistet.

## Was das Programm macht
- pingt alle Adressen eines IPv4-Netzwerks an (z. B. `192.168.0.0/24`)
- arbeitet mit 50 Pings gleichzeitig, damit ein Heimnetz in wenigen Sekunden durchsucht ist
- zeigt zu jeder gefundenen IP-Adresse den Gerätenamen, wenn das Netzwerk einen kennt
- funktioniert unter Windows, macOS und Linux
- prüft die Eingabe und lehnt ungültige oder zu große Netzwerke (größer als /22) ab

## Starten
```
python netzwerk_scanner.py 192.168.0.0/24
```

Die passende Netzwerkadresse findest du unter Windows mit `ipconfig`, unter macOS und Linux mit `ip a` bzw. `ifconfig`.

Beispielausgabe:
```
Scanne 192.168.0.0/24 ...

IP-Adresse        Name
----------------------------------------
192.168.0.1       router.local
192.168.0.23      laptop.local

2 Gerät(e) erreichbar.
```

## Wichtig
Nur im eigenen Netzwerk verwenden oder dort, wo man ausdrücklich die Erlaubnis dazu hat.

## Benötigt
- Python 3.9 oder neuer
- keine zusätzlichen Pakete, nur die Standardbibliothek
