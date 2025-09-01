# System Instability Issues

![Issue_Types](.\images\Instability.png)

die Probleme mit der Systeminstabilität:



Dazu gehören Probleme:
- mit dem Speicher,
- mit beschädigten Systemdateien
- mit USB-Geräten.



Systeminstabilität : das System einfriert, herunterfährt, nicht mehr reagiert, neu startet oder sich ohne Fehlermeldung ausschaltet.
![Issue_Types](.\images\Instability1.png)

![Issue_Types](.\images\Instability2.png)
In beiden Fällen handelt es sich in der Regel entweder  um ein Hardware- oder ein Software-Problem.

Hardwareprobleme: 
- Überhitzungsproblem, 
- Stromproblem 
- Problem mit dem Prozessor oder dem Speicher.

![Issue_Types](.\images\Instability4.png)

Softwareproblem:
- die Kerneldateien beschädigt sind und Windows mitten im Betrieb abstürzt, und dann wird das System neu gestartet oder heruntergefahren.



zu überprüfen: 

- Speicherdiagnose, 
- Systemdatei-Überprüfer
- Überprüfung der USB-Geräte.

![Issue_Types](.\images\Instability5.png)

## 1. eine Speicherdiagnose durchführen .

In Windows ist bereits ein Tool eingebettet,"Windows-Speicherdiagnosetool" 

![Issue_Types](.\images\Instability6.png)

![Issue_Types](.\images\Instability8.png)

Systemsteuerung --> Verwaltungstools 
oder 
Sie die Windows-Wiederherstellungsumgebung neu und wählen  Sie dann das Speicherdiagnosetool aus.

Sobald Sie das getan haben, startet Ihr Computer neu und  beginnt mit dem Test, um jeden einzelnen Teil Ihres Speichers zu überprüfen.

Wenn Sie festgestellt haben, welches Speichermodul defekt ist, können sie es durch ein bekanntermaßen gutes Modul ersetzen und den Test erneut durchführen, um zu  überprüfen, ob das System vollständig korrigiert wurde  und der Speicher nun einwandfrei funktioniert.

![Issue_Types](.\images\Instability9.png)

![Issue_Types](.\images\Instability10.png)

## eventuell beschädigte System- oder Kerneldateien.

System File Checker, 

![Issue_Types](.\images\Instability12.png)

. sfc /scannow

![Issue_Types](.\images\Instability13.png)

. sfc /verifyonly

![Issue_Types](.\images\Instability14.png)

Es ist wichtig zu wissen, dass sfc alle Systemdateien überprüft, unabhängig davon, auf welchem 
Laufwerk sie gespeichert sind. Sie müssen also keinen Laufwerksbuchstaben wie Festplatte C oder Solid-State-Gerät C angeben.



. sfc /scanfile <PatrhToFile>

![Issue_Types](.\images\Instability15.png)

. sfc /verifyfile v<PatrhToFile>

![Issue_Types](.\images\Instability16.png)

## USB-Probleme.
![Issue_Types](.\images\Instability19.png)

Manchmal gibt es USB-Geräte, die nicht richtig funktionieren, sobald sie angeschlossen sind.

![Issue_Types](.\images\Instability17.png)

![Issue_Types](.\images\Instability18.png)



Dazu gehören z. B. Mäuse, Tastaturen,  Kopfhörer, Webcams, Drucker und andere USB-Geräte.

Denken Sie daran, dass es sich bei einem USB-Gerät um ein Hardware-Gerät handelt, das eine ordnungsgemäße Kommunikation
über den USB-Bus benötigt, um mit dem Computer zusammenzuarbeiten, aber der Computer muss auch über die richtigen
Treiber verfügen, um mit diesem Hardware-Gerät zu kommunizieren.


In diesem Fall sollten Sie überprüfen,  ob Sie die neuesten Treiber für Ihren USB-Bus oder Controller haben 
und ob der USB-Bus nicht versucht, in eine Art Energiesparmodus zu wechseln, der dann

- verwende  ***Windows Update-Tool** 
- müssen Sie im ***Gerätemanager jedes USB-Host-Controller-Gerät*** deinstallieren und dann den Computer neu starten, wodurch eine  Neuinstallation mit dem neuen Treiber erzwungen wird.
- enn das Ihr Problem nicht behebt, die ***selektive USB-Energieverwaltung*** entweder für einen
bestimmten Anschluss oder ein Gerät oder für das gesamte System deaktivieren.

