# Programmbeschreibung

## Produkt

`HVVMResourceMetering` ist eine Windows-Anwendung zur Messung von Hyper-V-Ressourcen auf dem lokalen Host.

Aktuelle Release-Version: `013`

## Hauptfunktion

Die Anwendung:

- aktiviert `VMResourceMetering` fuer alle lokalen Hyper-V-VMs
- misst waehrend der Laufzeit zusaetzlich empfohlene Hyper-V-Host-PerfCounter
- beendet die Messung kontrolliert per Button
- schreibt standardmaessig einen kompakten JSON-Report mit wichtigen Messwerten fuer Prozessor, Speicher, Netzwerk und Storage
- verarbeitet Host-PerfCounter robuster, auch wenn PowerShell einzelne Werte als Text oder `null` liefert
- protokolliert alle Aktionen in eine Logdatei

## Bedienung

Die Anwendung besitzt vier Buttons:

- `Start`
- `Stop`
- `JSON oeffnen`
- `Exit`

Zusaetzlich gibt es die Checkbox:

- `All Measure`

Die Oberflaeche ist im Stil von WinUI 3 mit eckigen Buttons, kleineren Ueberschriften und untereinander angeordneten Bereichen fuer Ergebnis und Log aufgebaut.

## Ausgabe

Es werden erzeugt:

- ein Logbereich in der Anwendung
- ein Ergebnisbereich in der Anwendung
- Logdateien im Ordner `logs`
- JSON-Reports im Ordner `reports`

Optional kann ueber `All Measure` die vollstaendige `Measure-VM`-Ausgabe zusaetzlich in die JSON-Datei aufgenommen werden.

## Voraussetzungen

- Windows mit Hyper-V-Rolle
- lokaler Start direkt auf dem Hyper-V-Host
- Hyper-V PowerShell-Modul
- empfohlen: administrative Rechte

## Release-Inhalt

Das Release enthaelt:

- die lauffaehige Windows-Anwendung
- die zugehoerige NLog-Konfiguration

Die Konsolenvariante wird nicht mehr verwendet.
