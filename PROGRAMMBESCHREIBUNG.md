# Programmbeschreibung

## Produkt

`HVVMResourceMetering` ist eine Windows-Anwendung zur Messung von Hyper-V-Ressourcen auf dem lokalen Host.

## Hauptfunktion

Die Anwendung:

- aktiviert `VMResourceMetering` fuer alle lokalen Hyper-V-VMs
- misst waehrend der Laufzeit zusaetzlich empfohlene Hyper-V-Host-PerfCounter
- beendet die Messung kontrolliert per Button
- schreibt einen kompakten JSON-Report mit den eigentlichen Messergebnissen
- protokolliert alle Aktionen in eine Logdatei

## Bedienung

Die Anwendung besitzt vier Buttons:

- `Start`
- `Stop`
- `JSON oeffnen`
- `Exit`

## Ausgabe

Es werden erzeugt:

- ein Logbereich in der Anwendung
- ein Ergebnisbereich in der Anwendung
- Logdateien im Ordner `logs`
- JSON-Reports im Ordner `reports`

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
