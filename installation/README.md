# Bemerkungen zur Dualbootinstallation auf Acer-Laptops

Acer ist der Ansicht, dass nur von Ihnen ausgesuchte Betribessysteme bootfähig sein sollen.
Da das vor allem im Dualboot mit Windows und Unix-OS zu Problemen führt, hier zusammengefasst was man machen kann. Der erste Weg funktioniert bei einer Platte, oder mehreren Platten, wenn die EFI-Partition auf der ersten Platte liegt. Dann klappt es auch bei einer Dualboot-Installation.

Quelle: https://wiki.ubuntuusers.de/EFI_Problembehebung/, abgerufen 15.08.18

### 1. Weg
Vor der Installation:
 - UEFI mit `F2` aufrufen
 - Touchpadmodus auf **Basic** stellen
 - `Security` → `Set Supervisor Password`
    - Vorschlag *passwort*, wird nach der Installation wieder entfernt
 - `Boot`
    - Modus: **UEFI**
    - Secure Boot: **enabled**
 - mit `F10` und *yes* verlassen

Die Installation läuft wie gewohnt ab.

Nach der Installation, beim ersten Start:
 - USB-Stick entfernen
 - UEFI mit `F2` aufrufen
 - Passwort eingeben, z.B. *passwort*
 - `Security` → `Select an UEFI file as trusted for executing` → `HDD0` → `EFI` → `<ubuntu>` → `shimx64.efi`
 - Supervisor Password wieder entfernen
 - mit `F10` und *yes* verlassen

### 2. Weg

Diesen Weg habe ich nicht selber getestet, er hat letztes Jahr, 2017, wohl funktioniert.

Link: https://askubuntu.com/questions/627416/acer-aspire-e15-will-not-dual-boot, abgerufen 15.08.2018
