# Application and Service issues

![appcrs](.\images\appcr.png)

# 1 Anwendungsprobleme

Wenn eine Anwendung abstürzt, sollte  es Ihre Priorität sein, so viele Daten wie möglich zu retten. 
Das Beste, was Sie tun können, um Probleme  beim Absturz von Anwendungen zu vermeiden, ist also,

Dateien regelmäßig zu speichern.
![appcrs](.\images\appcr1.png)

![appcrs](.\images\appcr2.png)


Darüber hinaus verfügt Windows über eine Funktion, die als  Windows-Dateiverlauf bekannt ist und die Sie aktivieren können, sowie über Funktionen innerhalb von OneDrive, einem Cloud-Speicherdienst, der als kontinuierliche Sicherung für verschiedene Dateiversionen fungieren  kann, während Sie an diesen Dateien  arbeiten.

![appcrs](.\images\appcr3.png)


## APPs ISSUSES
1. Wann immer eine Anwendung bei Ihnen einfriert und nicht  mehr reagiert, 
- sollten Sie versuchen, ihr zunächst Zeit zu geben, um ihre Arbeit zu beenden.
Wenn Sie dem Prozess ***etwas Zeit geben***, wird er vielleicht wieder ansprechbar, und  dann können Sie die Daten, an denen Sie gearbeitet  haben, speichern oder wiederherstellen.

2. Wenn er einfriert oder über einen längeren Zeitraum nicht mehr reagiert, haben Sie möglicherweise keine andere 
- Wahl, als den ***Task-Manager*** zu öffnen und den Prozess oder das Programm zu beenden, 
um wieder Zugriff auf den gesamten Computer zu erhalten.
![appcrs](.\images\appcr4.png)

3. Wenn Sie feststellen, dass dieselbe Anwendung häufig abstürzt, könnte  dies ein Problem mit dieser Anwendung oder den ihr zugrunde liegenden Konfigurationsdateien sein.

- Sie zunächst beim Hersteller nachsehen, ob es eine aktualisierte Version der Software gibt, denn normalerweise deutet dies auf eine Beschädigung des Programms oder eine Schwachstelle hin, die ausgenutzt wird.

In diesen Fällen ist das Problem normalerweise durch ein  ***Update*** auf die neueste Version gelöst.

![appcrs](.\images\appcr5.png)

4. Wenn das Update das Problem nicht behebt, könnte  es sein, dass das zugrunde liegende Programm selbst beschädigt wurde.

- sollten Sie das Programm deinstallieren, den Computer neu starten und das Programm dann neu installieren.  Dadurch können Sie das Programm normalerweise ***neu installieren***  und sicherstellen, dass alle Dateien in den ursprünglichen Zustand zurückversetzt sind,  was viele Probleme mit dem Absturz der Anwendung lösen kann.

![appcrs](.\images\appcr6.png)

![appcrs](.\images\appcr7.png)


![appcrs](.\images\appcr8.png)

## 2 Services
Services: eine ganze Reihe von Programmen, die im Hintergrund laufen, ohne dass Sie es merken.

![appcrs](.\images\appcr9.png)

Wenn jedoch einer dieser Dienste nicht gestartet wird,  kann dies zu Problemen führen, nachdem  Sie Ihren Windows-Rechner hochgefahren haben. 

Um festzustellen, ob einer dieser Dienste nicht gestartet werden konnte, können 
Sie in der Ereignisanzeige nachsehen, warum der Start fehlgeschlagen ist, oder Sie können das Dienste-Tool öffnen, um festzustellen,  welcher Dienst nicht gestartet werden konnte.

![appcrs](.\images\appcr10.png)

Wenn Sie festgestellt haben, welcher Dienst nicht gestartet werden konnte, besteht der erste Schritt  zur Fehlerbehebung darin, diesen Dienst manuell zu starten.

Im Dienste-Tool identifizieren Sie den Dienst, klicken ihn mit der rechten Maustaste an und dann auf Starten. 
Dadurch kann dieser Dienst gestartet werden. 
![appcrs](.\images\appcr11.png)


Wenn dieser Dienst nicht gestartet wird. Das kann bedeuten, dass ein größeres Problem im Spiel ist. Oft sind diese Dienste miteinander verknüpft und arbeiten zusammen.

![appcrs](.\images\appcr12.png)
![appcrs](.\images\appcr13.png)

Wenn Sie also festgestellt haben, welcher Dienst nicht startet, sollten  Sie auf der Microsoft-Website nach  Informationen über  diesen Dienst suchen, um festzustellen, welche anderen Dienste mit ihm verknüpft sind.

Wenn Sie zum Beispiel drei Dienste haben,  nennen wir sie A, B und C. Und A kann jederzeit starten, B kann jederzeit starten, aber  C kann nicht starten, bevor A nicht gestartet ist.



Und manchmal werden Sie feststellen, dass einige Dienste  tatsächlich mit anderen Diensten in Konflikt geraten.
Nehmen wir zum Beispiel an, es gäbe einen Dienst, der Ihrem Gehirn sagt, welche Sprache Sie sprechen sollen.
Wenn Sie nun einen Dienst haben, der sich einschaltet und sagt, dass Sie Englisch sprechen werden, und einen anderen, der sich  einschaltet und sagt, dass Sie Spanisch sprechen werden, dann können nicht beide gleichzeitig arbeiten, weil Sie nur einen Mund und eine Zunge
![appcrs](.\images\appcr14.png)

Und wenn Sie konkurrierende Dienste haben, müssen Sie einen Dienst deaktivieren, um den anderen einschalten zu können.

Ein weiteres Problem, das bei Diensten auftreten kann, ist, dass ein Dienst versucht, mit der falschen  Berechtigungsstufe zu laufen.

In diesem Fall haben Sie nicht genügend Berechtigungen. Wir müssen also sicherstellen, dass der Dienst über ausreichende Berechtigungen verfügt, um das zu tun, was er tun muss, und dass das Konto, unter dem er läuft, die richtigen Berechtigungen hat, um das zu tun, was erforderlich ist.




Wenn ein zentraler Fensterdienst nicht funktioniert, ist das in der Regel ein Zeichen für eine Malware-Infektion oder 
eine Systembeschädigung.
![appcrs](.\images\appcr15.png)
![appcrs](.\images\appcr16.png)

In diesen Fällen sollten Sie Ihr Systemdatei-Überprüfungsprogramm verwenden, um sicherzustellen, dass alle  Systemdateien intakt sind und sich keine Malware oder Infektionen darauf befinden.


Wenn ein Dienst nicht ausgeführt werden kann, kann es sein, dass die von ihm verwendete Dynamic-Link-Bibliothek nicht 
richtig registriert ist. In diesen Fällen verwenden Sie das Programm regsvr32, das für Registry Server Program 
steht, um die Softwarekomponente zu registrieren

und sicherzustellen, dass die Dynamic-Link-Library oder DLL, auf die sich der Dienst stützt, ordnungsgemäß mit dem Dienst verknüpft ist.
![appcrs](.\images\appcr17.png)
![appcrs](.\images\appcr18.png)


## 3 die Zeitverschiebung sprechen.
![appcrs](.\images\appcr19.png)
![appcrs](.\images\appcr20.png)
![appcrs](.\images\appcr21.png)

Darüber hinaus stützen sich viele Netzwerkdienste auf das so genannte Network Time Protocol, mit dem Sie die Zeit aller Geräte im Netzwerk synchronisieren können.

Ich kann also von meinem Domänencontroller oder meinem Netzwerkzeitserver aus eine Aktualisierung an alle mit mir verbundenen Personen senden, so dass wir alle die gleiche Zeit verwenden.

Aber letztendlich wird auf jedem Computer die Zeit zwischen diesen Zeitsynchronisationen mit Hilfe der Echtzeituhr und dieser kleinen Batterie, die in der Hauptplatine eingebaut ist, gehalten.

I