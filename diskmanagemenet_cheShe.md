<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# ja bitte  **optimierte Checkliste im Kurzformat** machen

Perfekt 👍 – hier eine **optimierte Kurz-Checkliste (Cheat-Sheet) für IT-Admins** zum Thema **Datenträgerverwaltung unter Windows (GUI \& DiskPart)**.
Ich habe sie bewusst kompakt gehalten, so dass du sie wie eine kleine Referenzkarte neben dem Monitor haben kannst:

***

# 🖥️ Windows Datenträgerverwaltung – Admin-Cheat-Sheet

## 1. Vorbereitung

- 📌 **Ziel festlegen**: OS, Daten, Backup, VM, RAID?
- 📌 **Backup erstellen**, bevor gelöscht/konvertiert wird.
- 📌 Hardware checken (BIOS/UEFI, Schnittstelle, Firmware).

***

## 2. Initialisierung

- **GUI**: Rechtsklick → „Datenträger initialisieren“.
- **DiskPart**:

```
list disk
select disk <N>
convert gpt     # oder convert mbr
```


***

## 3. Partition anlegen

- **GUI**: Unallocated → „Neues Volume“.
- **DiskPart**:

```
select disk <N>
create partition primary [size=<MB>]
```


***

## 4. Formatieren \& Laufwerksbuchstabe

- **GUI**: „Formatieren“ (NTFS/exFAT/ReFS), Laufwerksbuchstabe wählen.
- **DiskPart**:

```
select partition <N>
format fs=ntfs quick label=<Name>
assign letter=<X>
```


***

## 5. Bootfähig machen (nur MBR)

```
select partition <N>
active
```

➡️ GPT/UEFI: EFI-Systempartition automatisch verwendet.

***

## 6. Prüfen

```
list disk
list partition
list volume
detail disk / partition / volume
```


***

## 7. Volume-Größe ändern

- **GUI**: Rechtsklick → "Erweitern..." / "Verkleinern..."
- **DiskPart**:

```
select volume <N>
extend [size=<MB>]
shrink desired=<MB>
```


⚠️ BitLocker → vorher deaktivieren/entsperren.

***

## 8. Attribute \& Status

- Schreibschutz:

```
select disk <N>
attributes disk set readonly / clear readonly
```

- Online/Offline (Cluster/SAN wichtig!):

```
offline disk
online disk
```


***

## 9. MBR ↔ GPT umwandeln

- **Achtung: Datenträger muss leer sein!**

```
select disk <N>
clean
convert gpt / mbr
```

💡 Alternative: `mbr2gpt.exe /convert /allowFullOS`

***

## 10. Bereinigen

- Schnell löschen:

```
clean
```

- Sicheres Löschen:

```
clean all
```


***

## 11. Dynamische Datenträger (Legacy)

```
convert dynamic
create volume simple / spanned / stripe / mirror
```

➡️ Heute oft durch **Storage Spaces** oder HW-RAID ersetzt.

***

## 12. Abschluss

- Neustart, wenn Boot-Partition geändert wurde.
- Explorer-Test: Dateien erstellen/lesen.
- Dokumentation: Größen, Buchstaben, Verwendungszweck notieren.

***

✅ **Best Practices für Admins**

- OS, Apps, Logs, Daten auf **getrennten Volumes**.
- Für Server: NTFS oder ReFS (Storage Spaces).
- SSD → Alignment automatisch ok, TRIM aktiv lassen.
- Rechenzentrum: „clean“ für Wiederverwendung, „clean all“ nur für Entsorgung.

***

👉 Damit hast du eine ultrakompakte Übersicht für den Alltag als Systemadministrator.

Möchtest du, dass ich daraus noch eine **druckfertige PDF im Poster/Quick-Reference-Stil** formatiere (eine Seite mit Boxen \& Highlighting)?

