---
title: Einfache Hacks für mehr Effizienz und Selbstbedienung - Teil 1
description: Lernen Sie die wichtigsten Herausforderungen kennen, mit denen Analyseteams heute konfrontiert sind, und lernen Sie unsere Empfehlungen kennen, um sie mithilfe von Strategien außerhalb der Adobe Analytics-Benutzeroberfläche zu überwinden.
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: dad200fdb5c5d15c00254d693fb47bbcec80afaf
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Adobe Analytics: Einfache Hacks für mehr Effizienz und Selbstbedienung

**Teil 1: Außerhalb der Benutzeroberfläche**

In diesem Artikel werden die wichtigsten Herausforderungen beschrieben, vor denen Analyseteams heute stehen, sowie unsere Empfehlungen zur Überwindung dieser Herausforderungen mithilfe von Strategien außerhalb der Adobe Analytics-Oberfläche.

## Wichtige Herausforderungen für Analytics-Teams

Viele Analytics-Teams haben eine unausgewogene Arbeitsverteilung. Anstelle einer Mischung aus 80 % Analyse und 20 % Implementierung finden sich zahlreiche Unternehmen im Umkehrschluss davon. Sie sehen die meisten ihrer Anstrengungen, die sie mit der Einrichtung, Berichterstellung und Bereitstellung von Unterstützung unternommen haben, im Gegensatz zur Produktion von Analysen, die wertvolle Einblicke liefern.

Für Analytics-Teams sind Produktivität und Effizienz aus verschiedenen Gründen beeinträchtigt. Dazu gehören die sich ständig ändernden und sich entwickelnden Implementierungen, der Versuch, das Vertrauen der Organisation in die Daten zu erhalten und den Analyseumsatz zu reduzieren. Durch die Umsatzreduzierung wird der langwierige Prozess der Ausbildung neuer Teammitglieder zu unbekannten, benutzerdefinierten Implementierungswerkzeugen vermieden.

Andere wichtige Herausforderungen für Analysten:

* **Wettbewerb:** Online- und Mehrkanal-Einzelhandelsunternehmen werden wettbewerbsfähiger.
* **Kundenerwartungen:** Kundenerlebnisse und Marketingstrategien werden komplexer.
* **Datenwert:** Der Wert genauer Daten und Einblicke zur Förderung eines Wettbewerbsvorteils wird immer wichtiger.
* **Erwartungen der Interessenträger:** Geschäftspartner, Interessengruppen und Führungskräfte fordern immer häufiger Daten vor der Genehmigung an.
* **Projektmanagement:** Das Analytics-Team nimmt die Anforderungen zur Implementierung der Datenerfassung für einen nie endenden Strom neuer Funktionen auf, generiert präzise Berichte, Onboarding neuer Analysten und Aufdecken der nächsten neuen Einblicke.

## Schlüssel zur Effizienz: Außerhalb der Benutzeroberfläche

1. Halten Sie Ihre [Lösungsdesign-Referenz](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SZR) Aktuell:

   * Die SDR ist die primäre &quot;Source of Truth&quot; für die Definition und beabsichtigte Verwendung aller Variablen in Ihrer Analytics-Implementierung.
   * Die SDR ist die Hauptreferenz, mit der Benutzer vertraut sein müssen, um die Adobe Analytics-Benutzeroberfläche optimal zu nutzen.
   * Es muss aktualisiert und versioniert werden (es kann ein einfaches Datumsformat verwendet werden).

1. Dokumentation zur Datenerfassung und Governance - Technische Spezifikationen:

   Die technische Spezifikation hat eine eingeschränktere Zielgruppe als die SDR, ist jedoch für eine voll funktionsfähige Implementierung ebenso wichtig, wenn nicht sogar wichtiger. Eine gute technische Spezifikation sollten alle Entwicklungs-, QA- und Tag-Management-Ressourcen sein, die zur Implementierung der Lösung erforderlich sind. Stellen Sie sicher, dass Sie so viele Dokumente verwalten, wie Sie benötigen, um einzigartige Implementierungsarchitekturen aufzunehmen.

   **Tech Spec**

   _Anwendungsbeispiel:_ Anweisungen zum Erstellen von Skripten für die Datenerfassung

   _Primäre Benutzer:_ Entwickler

   _Weitere Hinweise:_

   * Hochtechnisches Dokument, das speziell für Ihre Bereitstellungsumgebungen erstellt wurde
   * Nützlich für die erstmalige Implementierung und die anschließende Wartung/Referenz
   * Organisiert nach Lösungstyp (z. B. Kampagnen-Tracking, Seitenmetadaten usw.)
   * Primäres Dokument muss aktualisiert und gepflegt werden, wenn SDR-Änderungen vorgenommen werden.
   * Zentrales Repository
   * Synchronisierte Versionsnummern für SDR und Tech Spec

1. Design-Absicht für Kommunikation und Dokumentenlösung beim Start:

   * Kommunikation mit dem Benutzer im Hinterkopf
   * Erstellen Sie beim Start oder bei der Erweiterung der Datenerfassung einfache Zusammenfassungen, die für Interessengruppen freigegeben werden können.
   * Eigene Variablenverwendung außerhalb des Gate-Moduls verstärken
   * Senden Sie eine zusammenfassende Launch-Ankündigung per E-Mail an die wichtigsten Interessengruppen und Analysten.
   * Erstellen Sie eine Bibliothek, die zur Unterstützung von Bürozeiten, Team-Aktivierungssitzungen oder für Team-spezifisches Onboarding verwendet werden kann.

1. Dokumentation zur Datenerfassung, Governance und Datenhygiene - AHD:

   Das Analytics Health Dashboard (AHD) taucht tief in ein _single_ Report Suite und bietet eine Ansicht der Daten, die in jeder Komponente erfasst werden (eVar, Eigenschaft und Ereignis). Dies kann Ihnen dabei helfen, herauszufinden, ob die Datenerfassung in einer Komponente beendet wurde, damit Sie Maßnahmen ergreifen können, um das Problem zu beheben. Sie können dieses Dashboard für jede Report Suite jederzeit ausführen.

   Analytics Health Dashboard (AHD):

   _Anwendungsbeispiel:_ Momentaufnahme aller Metriken und Dimensionen, die von einer einzelnen Report Suite erfasst werden

   _Primäre Benutzer:_ Lead Analytics-KMU und/oder Entwickler

   _Weitere Hinweise:_
   * Wird über Excel mithilfe einer benutzerdefinierten Integration der Adobe Reporting-API bereitgestellt
   * Benutzer müssen Zugriff auf die Analytics Web Services API haben
   * Es gibt Optionen zur halbautomatischen Ausführung

1. Gewinnen Sie durch die Erweiterung der Welt der Fachexperten (KMU):

   * Gründung von KMU in den verschiedenen Teams der Organisation
   * Erstellen Sie ihre Präsenz, indem Sie Veröffentlichungen und Gewinne sozialisieren
   * Verwenden Sie reguläre Bürozeiten, um die Trainer zu schulen und Ad-hoc-Aufgaben zu reduzieren.

Erfahren Sie mehr über Strategie und Gedankenführung auf der [Kundenerfolg](https://experienceleague.corp.adobe.com/docs/customer-success/customer-success/overview.html) Hub.