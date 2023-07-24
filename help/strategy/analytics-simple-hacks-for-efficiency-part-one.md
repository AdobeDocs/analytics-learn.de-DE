---
title: Einfache Hacks für mehr Effizienz und leichtere Selbstbedienung – Teil 1
description: Lernen Sie die wichtigsten Herausforderungen kennen, mit denen Analytics-Teams heute konfrontiert sind, und lernen Sie unsere Empfehlungen kennen, um sie mithilfe von Strategien außerhalb der Adobe Analytics-Benutzeroberfläche zu überwinden.
feature: Analytics Basics
role: Admin, Leader
level: Intermediate
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: d7fd77640928697f5857ccfcaf2c0f561aebeac3
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 100%

---

# Adobe Analytics: Einfache Hacks für mehr Effizienz und leichtere Selbstbedienung

**Teil 1: Außerhalb der Benutzeroberfläche**

In diesem Artikel werden die wichtigsten Herausforderungen beschrieben, vor denen Analytics-Teams heute stehen, sowie unsere Empfehlungen zur Überwindung dieser Herausforderungen mithilfe von Strategien außerhalb der Adobe Analytics-Oberfläche.

## Wichtige Herausforderungen für Analytics-Teams

In vielen Analytics-Teams gibt es eine unausgewogene Arbeitsverteilung. Anstelle einer Mischung aus 80 % Analyse und 20 % Implementierung ist es bei zahlreiche Unternehmen umgekehrt. Sie stellen fest, dass die meiste Zeit für das Einrichten, Erstellen von Berichten und Bereitstellen von Support aufgewendet wird und nicht für die Erstellung von Analysen, die zu wertvollen Erkenntnissen führen.

Analytics-Teams stellen fest, dass ihre Produktivität und Effizienz aus verschiedenen Gründen abnimmt. Dazu gehören die sich ständig ändernden und weiterentwickelnden Implementierungen und der Versuch, das Vertrauen der Organisation in die Daten aufrechtzuerhalten sowie die Fluktuation der Analyst*innen zu verringern. Durch die Reduzierung der Fluktuation wird der langwierige Prozess der Ausbildung neuer Team-Mitglieder im Umgang mit ihnen unbekannten Werkzeugen zur benutzerdefinierten Implementierung vermieden.

Andere wichtige Herausforderungen für Analyst*innen:

* **Wettbewerb:** Online- und Mehrkanal-Einzelhandelsunternehmen werden immer wettbewerbsfähiger.
* **Kundenerwartungen:** Kundenerlebnisse und Marketing-Strategien werden immer komplexer.
* **Datenwert:** Es wird immer wichtiger, genaue Daten und Erkenntnisse zu haben, um einen Wettbewerbsvorteil zu erzielen.
* **Erwartungen der Stakeholder:** Geschäftspartner, Stakeholder und Führungskräfte fordern zunehmend Daten an, bevor sie ihre Zustimmung geben.
* **Projekt-Management:** Das Analytics-Team wird mit Anfragen überhäuft, die Datenerfassung für einen nicht enden wollenden Strom neuer Funktionen zu implementieren und gleichzeitig genaue Berichte zu erstellen, neue Analyst*innen einzubinden und die nächste neue Erkenntnis zu gewinnen.

## Schlüssel zur Effizienz: Außerhalb der Benutzeroberfläche

1. Halten Sie Ihre [Lösungs-Design-Referenz](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SDR) auf dem neuesten Stand:

   * Die SDR ist die primäre Informationsquelle für die Definition und beabsichtigte Verwendung aller Variablen in Ihrer Analytics-Implementierung.
   * Die SDR ist die Hauptreferenz, mit der Benutzer*innen vertraut sein müssen, um die Adobe Analytics-Benutzeroberfläche optimal zu nutzen.
   * Sie muss regelmäßig aktualisiert und versioniert werden (dazu kann ein einfaches Datumsformat verwendet werden).

1. Dokumentation zur Datenerfassung und Governance – Technische Spezifikationen:

   Die technische Spezifikation hat eine stärker eingeschränkte Zielgruppe als die SDR, ist jedoch für eine voll funktionsfähige Implementierung mindestens ebenso wichtig. Eine gute technische Spezifikation sollte alle Ressourcen für die Entwicklung, Qualitätssicherung und das Tag-Management enthalten, die für die Implementierung der Lösung benötigt werden. Stellen Sie sicher, dass Sie so viele Dokumente verwalten, wie Sie benötigen, um einzigartige Implementierungsarchitekturen zu berücksichtigen.

   **Technische Spezifikation**

   _Anwendungsbeispiel:_ Anweisungen zum Erstellen von Skripten für die Datenerfassung

   _Primäre Benutzer*innen:_ Entwickler*innen

   _Weitere Hinweise:_

   * Hochtechnisches Dokument, das speziell für Ihre Bereitstellungsumgebungen erstellt wurde
   * Nützlich sowohl für die erstmalige Implementierung als auch die anschließende Wartung/Referenz
   * Organisiert nach Lösungstyp (z. B. Kampagnen-Tracking, Seitenmetadaten usw.)
   * Primäres Dokument, das aktualisiert und gepflegt werden muss, wenn Änderungen der SDR vorgenommen werden
   * Zentrales Repository
   * Synchronisierte Versionsnummern für SDR und technische Spezifikation

1. Kommunizieren und dokumentieren des beabsichtigten Lösungs-Designs bei der Einführung:

   * Kommunizieren Sie mit den Benutzer*innen im Hinterkopf
   * Erstellen Sie beim Start oder bei der Erweiterung der Datenerfassung einfache Zusammenfassungen, die mit Stakeholdern geteilt werden können
   * Legen Sie gleich von Anfang an Wert auf die richtige Verwendung von Variablen
   * Senden Sie eine E-Mail mit einer Zusammenfassung der Einführungsankündigung an die wichtigsten Stakeholder und Analyst*innen
   * Erstellen Sie eine Bibliothek, die zur Unterstützung außerhalb der Bürozeiten, Team-Aktivierungssitzungen oder für Team-spezifisches Onboarding verwendet werden kann.

1. Dokumentation zur Datenerfassung, Governance und Datenhygiene – AHD:

   Das Analytics Health Dashboard (AHD) taucht tief in eine _einzelne_ Report Suite ein und bietet eine Ansicht der Daten, die in jeder Komponente erfasst werden (eVar, Eigenschaft und Ereignis). Auf diese Weise können Sie feststellen, ob die Datenerfassung in einer Komponente gestoppt wurde, so dass Sie Maßnahmen ergreifen können, um das Problem zu beheben. Sie können dieses Dashboard für jede Report Suite jederzeit ausführen.

   Analytics Health Dashboard (AHD):

   _Anwendungsbeispiel:_ Momentaufnahme aller Metriken und Dimensionen, die von einer einzelnen Report Suite erfasst werden

   _Primäre Benutzer*innen:_ Lead Analytics-KMU und/oder Entwickler*innen

   _Weitere Hinweise:_
   * Wird über Excel mithilfe einer benutzerdefinierten Integration der Adobe Reporting-API bereitgestellt
   * Benutzer*innen müssen Zugriff auf die Analytics Web Services API haben
   * Es gibt Optionen zur halbautomatischen Ausführung

1. Gewinnen Sie durch die Erweiterung der Welt der Fachexpert*innen (SMEs):

   * Benennung von SMEs in den verschiedenen Teams der Organisation
   * Bauen Sie ihre Präsenz auf, indem Sie ihnen dabei helfen, Veröffentlichungen und Erfolge bekannt zu machen.
   * Nutzen Sie die regulären Bürozeiten, um bei der Schulung der Trainer*innen zu helfen und die Zahl der Ad-hoc-Anfragen zu verringern.

Erfahren Sie mehr über Strategie und Gedankenführung auf dem [Customer Success](https://experienceleague.adobe.com/docs/customer-success/customer-success/overview.html?lang=de)-Hub.