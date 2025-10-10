---
title: Ausführliches Handbuch für den Umstieg von Google Analytics auf Adobe Analytics
description: Erfahren Sie, wo äquivalente Funktionen zu finden sind und wie Sie diese beim Wechsel von Google Analytics zu Adobe Analytics effizient nutzen können.
feature: Third-party Integration
role: User
level: Beginner
kt: 9830
thumbnail: 34749.jpg
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '3403'
ht-degree: 97%

---

# Ausführliches Handbuch für den Umstieg von Google Analytics auf Adobe Analytics{#comprehensive-guide-for-transitioning-to-Adobe-Analytics}

## &#x200B;1. Einführung

Eine der größten Herausforderungen bei der Umstellung von einem Tool auf ein anderes besteht darin, zu lernen, wo die entsprechenden Funktionen zu finden sind und wie man sie effizient nutzt. Diese Ausführungen sind Teil einer umfangreicheren Anleitung, die Benutzern den Umstieg auf Adobe Analytics erleichtern soll (entweder als neuer Benutzer oder als jemand, der zuvor Google Analytics verwendet hat). Ein ausführlicher Vergleich mit GA (dem Vergleichs-Tool, mit dem wahrscheinlich die meisten Benutzenden vertraut sind) sollte Ihnen helfen, Ihr vorhandenes Wissen auf das neue Toolset anzuwenden. Wenn es keine anderen Möglichkeiten zum Üben gibt, hilft Ihnen das, den Einstieg zu finden und Frustrationen, die möglicherweise während dieser Zeit auftreten, zu reduzieren.

Lassen Sie uns kurz die Terminologie vergleichen:

| **Beschreibung** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Eine Ereignismetrik, die anzeigt, dass eine Seite (oder ein Bildschirm in einer Mobile App) angesehen wurde | Seitenansicht | Seitenansicht. |
| Eine Metrik, die eine Reihe von Interaktionen auf Ihrer Website oder Mobile App darstellt, welche im gleichen Zeitrahmen stattfinden | Besuch | Sitzung |
| Eine Metrik, die ein identifiziertes Gerät definiert (basierend auf mehreren Kriterien, einschließlich Cookies und anderen Verhaltensmustern, um Benutzerinformationen zu vereinen) | Unique Visitor | Benutzer |

## &#x200B;2. Die Benutzeroberfläche

Wenn Personen Adobe Analytics und Google Analytics vergleichen, äußern sie oft, dass die Adobe-Benutzeroberfläche zunächst abschreckend sei. Das stimmt, es ist aber – ob Sie es glauben oder nicht – eine Stärke und keine Schwäche. Adobe bietet eine breite Palette von Werkzeugen und große Flexibilität bei der Datenvisualisierung, sodass Sie viel mehr Freiheit in der visuellen Darstellung haben.

Beginnen wir mit dem „In-Site“-Reporting.

### 2.1. In-Site-Reporting

#### 2.1.1. Startbildschirm

Sowohl Adobe Analytics als auch Google Analytics bieten die Möglichkeit, die erste Ansicht, die ein Benutzer bei der Anmeldung sieht, anzupassen.

##### 2.1.1.1. Workspace / Benutzerdefinierter Startbildschirm (Adobe Analytics)

Adobe Analytics erstellt keinen vorgefertigten Bericht, der allen Benutzern bei der Anmeldung präsentiert wird. Die standardmäßige Startseite bringt Benutzende zum Startbildschirm für Workspace, auf dem für alle Benutzenden Workspace-Berichte angezeigt werden, die sie erstellt haben oder die für sie freigegeben wurden. Außerdem haben alle Benutzenden die Möglichkeit, einen dieser Berichte als Startbildschirm festzulegen, wenn sie dies möchten.

![workspace-create-project](assets/ga-to-aa_1.png)

Weitere Einzelheiten zu Workspace werden später in diesem Handbuch erläutert. Siehe Abschnitt 2.1.2.1

>[!TIP]
>
>Erstellen/Teilen Sie einige Standardberichte für Ihre Organisation, damit die Benutzer einen Ausgangspunkt haben, um Informationen zu sehen, ohne gleich ihre eigenen Berichte erstellen zu müssen.



##### 2.1.1.2. Startbildschirm-Einblicke (Google Analytics)

* Der Google Analytics-Startbildschirm bietet Ihnen einige vordefinierte Visualisierungen. Diese umfassen u. a. Folgendes:
* Benutzende, Sitzungen, Absprungrate und Sitzungsdauer in den letzten sieben Tagen
* Benutzer nach Tageszeit in den letzten 30 Tagen
* Aktuelle Benutzer und die aktivsten Seiten
* Traffic-Kanal, Quelle/Medium und Empfehlungen in den letzten sieben Tagen
* Sitzungen nach Land in den letzten sieben Tagen
* Top-Seiten der letzten sieben Tage
* Trend der aktiven Benutzer für die letzten 30 Tage
* und vieles mehr

Bei GA4 haben die Benutzer mehr Möglichkeiten, den Startbildschirm anzupassen und ihre eigenen Berichte hinzuzufügen.

![google-analytics-interfaces](assets/ga-to-aa_2.png)

Dies ist wahrscheinlich die Sache, die Sie in Adobe Analytics am meisten vermissen. Es gibt keinen vorgefertigten Startbildschirm für Sie. Sie können jedoch ganz einfach einen benutzerdefinierten Arbeitsbereich einrichten, um das zu replizieren, was Sie aus der obigen Liste benötigen, und diesen als Ihren Startbildschirm festlegen. Weitere Informationen zu diesem Thema finden Sie später (oder im Abschnitt 2.1.2.1 Adobe Workspace).

#### 2.1.2. In-Site-Berichterstellung

Zusätzlich zu den einfachen Berichten, die die Analyse-Tools bereitstellten, bietet jedes Tool auch leistungsfähigere Tools, mit denen Sie Ihre eigenen benutzerdefinierten Berichte erstellen können.

##### 2.1.2.1. Adobe Analytics Workspace

Dies ist das Kraftzentrale von Adobe Analytics. Seit seiner Einführung im Jahr 2017 ist es die erste Anlaufstelle für Analytics-Analysen und der Hauptgrund dafür, dass der Bereich „Berichte“ demnächst eingestellt wird.

Mit diesem Tool können Sie Berichte mit umfassender Freiheit erstellen.

Der Bericht kann in Bereiche unterteilt werden, die eine beliebige Anzahl von Visualisierungen enthalten können. Die Bereiche können auf allgemeine Informationen wie Datumsbereiche und allgemeine Segmentfilter eingestellt werden.

Sowohl die Bereiche als auch die darin enthaltenen Visualisierungen können in der Größe verändert und verschoben werden, um Elemente nebeneinander oder übereinander anzuzeigen. Wenn Sie also zwei verschiedene Datenreihen nebeneinander vergleichen möchten, können Sie Bereiche erstellen, die in der Mitte 50/50 geteilt sind und die beiden Sites nebeneinander zeigen, um einen einfachen Vergleich zu ermöglichen.

Benutzern steht eine Vielzahl von Visualisierungen zur Verfügung:

* Freiformtabelle
* Kohortentabelle
* Fallout
* Fluss
* Diagramme
   * Fläche (gestapelt und ungestapelt)
   * Linie
   * Streuung
   * Balken (gestapelt und ungestapelt)
   * Horizontales Säulendiagramm
   * Ringdiagramm
   * Histogramm
   * Horizontaler Balken (gestapelt und ungestapelt)
* Zuordnung
* Zusammenfassende Blöcke
   * Zusammenfassende Änderung
   * Zusammenfassender Text
   * Text (freies Textfeld zur Eingabe zusätzlicher Informationen, um den Kontext zu verdeutlichen)
* Venn

Jeder Bereich und jede Visualisierung kann betitelt und mit einer Beschreibung versehen werden, um den Kontext der angezeigten Informationen zu verdeutlichen.
In Adobe können Segmente (im Wesentlichen Filter für Daten) rückwirkend angewendet werden, und diese können in Spalten Ihrer Freiformtabellen übernommen werden, um Daten Seite an Seite zu vergleichen. Wenn ein Benutzer beispielsweise zwei verschiedene Kategorien auf seiner Website hinsichtlich der Besucherzahlen vergleichen möchte, kann er ein Segment für „Kategorie A“ und ein anderes Segment für „Kategorie B“ erstellen.

![analytics-page-views-report](assets/ga-to-aa_3.png)

Freiformtabellen ermöglichen mehrere Spalten und eine beliebige Segmentierung, um Daten nach Wunsch darzustellen.

Wenn Sie keine Aufschlüsselung nach Datum sehen möchten, ziehen Sie einfach per Drag-and-Drop eine andere Dimension oder ein Segment dorthin, um die Daten auf eine andere Weise anzuzeigen. Verwenden Sie beispielsweise Segmente für den Gerätetyp und fügen Sie dann eine Aufschlüsselung nach Betriebssystem für Ihre Mobile-/Tablet-Benutzenden hinzu:

![analytics-compare-page-views-report](assets/ga-to-aa_4.png)

Mit Workspace können Sie Ihrer Kreativität freien Lauf lassen, Sie sind nicht auf Standard-Aufschlüsselungen beschränkt. Sie können die Visualisierungen erstellen, die Sie benötigen, um aufschlussreiche Vergleiche auszuführen.

>[!TIP]
>
>Scheuen Sie sich nicht, zu spielen und zu forschen. Es gibt so viele Möglichkeiten, über den Tellerrand zu schauen. Überprüfen Sie außerdem, ob das, was Sie erstellt haben, auch das zeigt, was Sie vermuten. Erfahrung hilft!

Sie können ad-hoc berechnete Metriken oder Segmente erstellen, die nur innerhalb des Berichts verwendet werden, um zu verhindern, dass Ihr Segment- und Berechnungs-Repository überflutet wird. So können Sie zielgerichtete Elemente erstellen, die für bestimmte Berichte benötigt werden, ohne Ihr Unternehmen durch Dinge zu belasten, die in anderen Kontexten nicht verwendbar sind.

Diese Ausführungen sind nur eine Einführung in dieses Tool. Es existieren weitere umfassende Handbücher, die Ihnen den Einstieg erleichtern. Sobald Sie diese Handbücher durchgesehen haben, erstellen Sie umfassende Berichte wie den folgenden:

![workspace-dashboard](assets/ga-to-aa_5.png)

Arbeitsbereiche werden nicht automatisch gespeichert. So ist es einfacher, einen einmaligen Ad-hoc-Bericht zu erstellen, ohne das Repository Ihres Berichts zu verstopfen.

Ein weiteres leistungsstarkes Merkmal von Arbeitsbereichen ist die Möglichkeit, interaktive Modifikatoren in Form von Dropdown-Menüs auf Ihre Berichte anzuwenden. Diese Dropdown-Menüs funktionieren nicht bei exportierten CSV- oder PDF-Dateien Ihrer Berichte. Im Live-Bericht können Sie jedoch alle Visualisierungen in einem Bedienfeld aktualisieren, um denselben Bericht unter verschiedenen Bedingungen anzuzeigen. Es können mehrere Dropdown-Menüs verwendet werden. Solange sich die Optionen nicht gegenseitig ausschließen, werden die ausgewählten Elemente gestapelt, um eine übersichtliche Darstellung der Informationen zu ermöglichen.

>[!IMPORTANT]
>
>Weitere Informationen über die Verwendung von Dropdown-Menüs und Freiform-Aufschlüsselungen finden Sie unter <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: Dashboards, benutzerdefinierte Berichte und gespeicherte Berichte

Google verfügt über einige Tools zur Erstellung von Berichten innerhalb der Benutzeroberfläche, die jedoch die gleiche Darstellung und die gleichen Einschränkungen wie der Bereich mit den Berichten aufweisen.

Wer sich mit Google Analytics auskennt, wird sich jetzt vielleicht fragen, ob Google Data Studio nicht ein besseres Äquivalent zu Adobes Workspace ist. Ja, aber Data Studio ist technisch gesehen kein Teil des Analytics-Tools und ermöglicht Verbindungen zu verschiedenen Datenquellen. Dieses Tool wird später im Abschnitt „Erweiterter Zugriff auf Berichte“ behandelt, insbesondere in Abschnitt 2.2.3.

Google-Dashboards und benutzerdefinierte Berichte ermöglichen es Ihnen, mehrere Visualisierungen in einem Bericht zusammenzufassen. Im Gegensatz zu Workspace sind Sie aber immer noch auf einfache Korrelationen beschränkt und können nicht festlegen, welche Daten in welche Spalten eingefügt werden können.

Bei benutzerdefinierten Berichten besteht eine der größten Herausforderungen darin, dass ein Filter, den Sie erstellen, für alle Registerkarten des Berichts gilt. Es gibt keine Möglichkeit, zwei verschiedene Filter innerhalb desselben Berichts zu vergleichen.

Für Oberflächenvergleiche ist das jedoch kein Problem. All diese Funktionen ähneln denen der älteren Dashboards, benutzerdefinierten Berichten und Lesezeichen von Adobe. Grundlegende Tools zur Erfüllung Ihrer Anforderungen, die in der Report Suite enthalten sind.

#### 2.1.3. Berichte

Sowohl Google als auch Adobe verfügen über einige navigierbare Berichte, bei denen es sich um vorgefertigte Tabellen und einfache Zeitreihendiagramme handelt, die auf einer Dimension basieren.

##### 2.1.3.1. Adobe Analytics-Berichte

Adobe Analytics verfügt auch über einen Abschnitt „Berichte“, der jedoch schrittweise zugunsten von Analysis Workspace eingestellt wird. Tatsächlich wurde das Ende des Lebenszyklus für diese Benutzeroberfläche angekündigt, da Workspace ein leistungsfähigeres Tool ist. Die meisten dieser Tabellen können einfacher erstellt und geändert werden. Bei Adobe sind die Abschnitte viel stärker untergliedert, was entmutigend wirken kann:

![analytics-site-metrics](assets/ga-to-aa_6.png)

Da die meisten der oben genannten Punkte über Workspace zugänglich sind, gebe ich einen kurzen Überblick über diese Abschnitte und ihre Beziehung zu Google Analytics, und hebe die Berichte hervor, die hier noch relevant sind.

Website-Metriken sind das, was Sie erwarten würden, also die Standardmetriken (Seitenaufrufe, Unique Visitors, Besuche und benutzerdefinierte Ereignisse, die Sie eingerichtet haben). Dieser Bericht ähnelt dem Verhaltensbericht in GA, enthält aber auch einige der Informationen, die Sie unter „Zielgruppe“ finden würden (da Adobe die verschiedenen Metriktypen nicht aufteilt).

Hier finden Sie „Bot“-Berichte. Der Traffic von Bots wird von allen Standardberichten ausgeschlossen. Es gibt jedoch zwei Berichte, die Aufschluss darüber geben, was passiert und welche Bots auf Ihre Website kommen. Dies ist besonders nützlich, wenn Sie benutzerdefinierte Bot-Regeln eingerichtet haben, um bekannte Spam-Bots auszuschließen, die häufig Ihre Website besuchen. So erhalten Sie einen Einblick in die Aktivitäten dieser Bots, ohne dass Ihre Hauptberichte mit deren Traffic überflutet werden. Bot-Berichte sind derzeit nicht über Workspace verfügbar (aber neue Berichtsfunktionen, die in Kürze verfügbar sein werden, ermöglichen es Benutzenden, diese Informationen auch dort abzurufen).

Site-Content ist eine Gruppierung von Adobe-Standarddimensionen: Seitenname, Site-Abschnitte, Hierarchien, Server und mehr. Alle diese Dimensionen sind in Workspace verfügbar.

Mobile ist eine Gruppierung mobilgerätespezifischer Daten, einschließlich Geräten, Gerätetypen und mehr. Diese sind in Workspace verfügbar.

Pfade sind in Workspace nicht verfügbar. Workspace verfügt über ein Flussdiagramm, in dem Sie die Ein- und Ausgangsströme für eine einzelne Seite/einen einzelnen Wert sehen können. Im Gegensatz dazu können Sie mit „Paths“ die am häufigsten verwendeten Pfade in Ihrer Website anzeigen. Standardmäßig ist „Seiten“ der erste Pfadbericht, der für Sie eingerichtet wird. Sie können dieses jedoch für benutzerdefinierte Eigenschaften wie den Wert „Seitentyp“ aktivieren. Sie können sich die Pfade innerhalb der Seitentypen ansehen. Ein weiterer Punkt, der mir persönlich an der Funktion „Pfade“ gefällt, ist die einfache Art und Weise, in der die Informationen präsentiert werden... Das Flussdiagramm in Workspace kann (abhängig von der angezeigten Datenmenge) schnell überwältigend werden. Ich empfehle, beide auszuprobieren... beide haben ihren Nutzen und Wert, je nachdem, was Sie erreichen wollen. Es sollte beachtet werden, dass für „Flüsse“ jede Dimension verwendet werden kann, während die Pfadbestimmung in einer Prop in der Verwaltungskonsole eingerichtet werden muss.

Die Berichte über Traffic-Quellen, Kampagnen und Marketing-Kanäle ähneln alle dem Akquisebericht bei Google. Der Bericht über Traffic-Quellen konzentriert sich auf die tatsächlichen Referrer, der Bericht über Kampagnen konzentriert sich auf Ihre Kampagnen-Codes, und der Bericht über Marketing-Kanäle konzentriert sich ebenfalls auf Kampagnen-Codes, wendet aber zusätzlich eine von Ihnen festgelegte Logik an, wie die Informationen zu verarbeiten sind. Adobe bietet mehr Freiheit beim Einrichten von Regeln. Im Gegensatz dazu erledigt Google zahlreiche Dinge für Sie, und das bedeutet ein Umdenken. Standardmäßig beträgt die Attribution bei Google für Campaign-Codes sechs Monate. Die Attribution bei Adobe ist standardmäßig auf eine Woche eingestellt. Sie können dies zwar in Ihren Admin-Einstellungen ändern, aber in Workspace können Sie tatsächlich eine benutzerdefinierte Attribution auf jede Dimension anwenden, was Ihnen viel mehr spontanen Spielraum bietet.

Die Berichte zur Besucherbindung und zum Besucherprofil ähneln den Zielgruppenberichten in Google Analytics. Die Besucherbindung konzentriert sich eher auf die Häufigkeit der Wiederkehr, während das Besucherprofil eher auf die Geografie und Technologie der Nutzer ausgerichtet ist.

Benutzerspezifische Konversions- und Traffic-Berichte sind beide benutzerspezifische Dimensionsberichte. Konversionen sind eVars. Sie können für einen benutzerdefinierten Ablauf den Wert festlegen, wie Treffer, Besuch, Monat und Jahr. Dieser Wert bleibt für einen Benutzer für den konfigurierten Zeitrahmen persistent, es sei denn, er wurde überschrieben. Traffic-Variablen sind Props. Sie können diese auch für Pfadberichte oder als Listenelemente einrichten, wobei Mehrfachwerte auf der Grundlage eines von Ihnen gewählten Trennzeichens aufgeteilt werden.

„Medien“ ist z. B. für Videos oder Audiodateien, für die Sie ein spezielles Medien-Tracking eingerichtet haben.

„Benutzerdefinierte Berichte“ ist ein Bereich, in dem ein Benutzer die Spalten und Aufschlüsselungen, die er innerhalb der Berichtsschnittstelle erstellt hat, anpassen und als benutzerdefinierten Bericht speichern kann. Da Workspace jedoch, wie bereits erwähnt, so viel leistungsfähigere Aufschlüsselungen und Korrelationen ermöglicht, sollten alle benutzerdefinierten Anpassungen dort vorgenommen werden. Dies war eine gute Lösung, bevor es Workspace gab.

Der Abschnitt „Lesezeichen“ ähnelt den benutzerdefinierten Berichten, wo häufig verwendete Berichte in der Berichtsschnittstelle mit Lesezeichen versehen werden können, damit sie leichter gefunden werden können.

Dashboard war ein älteres Produkt, das es ermöglichte, Reportlets von Daten in einer Visualisierung zu kombinieren. Die Funktionalität in Workspace (Abschnitt 2.1.2.1) ist jedoch so viel einfacher zu handhaben, dass es nur noch als Zugangspunkt zu veralteten Berichten existiert, die neu erstellt werden sollten, bevor diese Funktion eingestellt wird.

Zielvorgaben ermöglichen es, einen Bericht zu erstellen, der auf einer Zielvorgabe innerhalb eines bestimmten Zeitraums basiert. Teams überwachen Kampagnen, um festzustellen, ob sie auf dem richtigen Weg sind, um ihre Traffic-Ziele zu erreichen.

Alle Berichte in diesem Bereich können nach mehreren metrischen Spalten und Dimensionen aufgeschlüsselt werden. Die Einfachheit der Visualisierungen und die dahinter stehende Logik, welche Elemente miteinander in Beziehung gesetzt werden können, können manchmal jedoch frustrierend sein.

##### 2.1.3.2. Google Analytics-Berichte

Google Analytics unterteilt diese Berichte in die folgenden Abschnitte: Echtzeit, Zielgruppe, Akquise, Verhalten und Gespräche (in GA3) und in Lebenszyklus (mit den Unterabschnitten Akquise, Interaktion, Monetarisierung, Kundenbindung) und Benutzende (mit den Unterabschnitten Demografie und Technik).

![google-analytics-interface-compare](assets/ga-to-aa_7.png)

Sie können diese Visualisierungen geringfügig anpassen, eine sekundäre Dimensionsaufschlüsselung hinzufügen, die Visualisierung ändern, einen Filter für die Daten erstellen und vieles mehr Sie können Ihre Anpassungen als gespeicherten Bericht speichern.

So erhalten Sie schnell und einfach Einblicke in Ihre Daten. Sie können jedoch nicht Dinge wie Benutzer mit Seitenaufrufen für eine Seite in derselben Tabelle vergleichen und Sie können nicht mehr als eine zusätzliche Dimension hinzufügen, um zusätzliche Daten zu sehen.

Diese Berichte eignen sich gut für die schnelle Analyse von Daten, aber wenn Sie wirklich in die Tiefe gehen müssen, stellen diese Einschränkungen ein Problem dar.

### 2.2. Erweiterter Zugriff auf Berichte

Zusätzlich zum „In-Site-Reporting“ bieten die meisten Tools erweiterte Funktionen, mit denen Sie Ihre Analyse außerhalb der Tools durchführen und etwas Individuelleres erstellen können.

#### 2.2.1. Adobe Analytics Report Builder (Microsoft® Excel-Erweiterung)

Workspace ist ein großartiges Tool, aber manchmal müssen Sie Ihre Daten in eine benutzerdefinierte Kalkulationstabelle übertragen, möglicherweise mit dem Ziel, mehrere Datenquellen miteinander zu verknüpfen. An dieser Stelle kommt Report Builder ins Spiel.

Report Builder ist ein Plug-in für Microsoft® Excel, mit dem Sie Verbindungen zu Ihren Adobe Analytics-Daten erstellen können, um tabellarische Daten zu erhalten, die Sie in Excel bearbeiten können. Um dies effizient zu nutzen, würden Sie in der Regel die Daten in einige Rohdaten-Registerkarten einlesen und dann Zellverweise in Excel verwenden, um die Daten aus diesen Registerkarten in einen einzigen konsolidierten Bericht einzulesen und dann Diagramme und Visualisierungen zu erstellen.

>[!NOTE]
>
>Report Builder verfügt über eine spezielle Zugriffsberechtigung, die auf Ihre Benutzer angewendet werden muss, damit sie auf dieses Plug-in zugreifen können. Diese Berechtigung sollte nur Benutzenden erteilt werden, die gelernt haben, wie man das Tool richtig verwendet.

#### 2.2.2. Adobe Analytics-API-Verbindung

Wenn Sie Adobe Analytics-Daten mit etwas anderem als Excel verarbeiten müssen und die verarbeiteten Daten einschließlich der Bot-Regel-Ausschlüsse benötigen, verwenden Sie die API von Adobe, um die Daten direkt abzurufen. Verarbeiten Sie dann die Daten mithilfe eines Skripts oder fügen Sie sie einer Datenbank hinzu, um sie mit einem anderen System zu verwenden.

Es sollte beachtet werden, dass die API nach wie vor Korrelationsdaten abruft, wobei die in der Abrufanfrage angegebenen Aufschlüsselungen und Segmente angewendet werden.

Adobes Workspace (Abschnitt 2.1.2.1) verwendet die -API zum Erstellen der Berichte. Wenn Sie in Workspace den Debugging-Modus aktivieren, werden die verwendeten API-Aufrufe genau angezeigt. Auf diese Weise können Sie Ihre API-Aufrufe schnell erstellen. Indem Sie Workspace zum Erstellen und Überprüfen der Daten verwenden, die Sie abrufen möchten, verwenden Sie diese API-Aufrufe, um die Daten an Ihre eigene Verarbeitung weiterzugeben.


#### 2.2.3. Google Analytics Data Studio

Wenn Sie weitergelesen haben, wissen Sie bereits, dass ich Data Studio als Äquivalent zu Workspace von Adobe erwähnt habe. Mit Data Studio können Sie Google Analytics-Daten, aber auch Daten aus anderen Quellen einlesen. Dies ist hilfreich, wenn Sie Ihre Analysedaten mit anderen erfassten Daten zusammenführen möchten. Bei Google Analytics gibt es jedoch die gleichen Visualisierungsbeschränkungen. Die Art und Weise, wie die Zeilen und Spalten aufgebaut sind, ist immer noch begrenzt.

Es ist immer noch ein leistungsstarkes Tool, und ich würde niemandem davon abraten, es zu verwenden. Meine persönliche Erfahrung ist, dass ich das unflexible Verhalten ziemlich einschränkend empfinde.


#### 2.2.4. Google Tabellen-Erweiterung

Für meine eigenen Zwecke, wenn ich erweiterte Daten von Google Analytics abrufen muss, ist mein persönliches Tool der Wahl die Google Tabellen-Erweiterung. Selbst wenn ich mehrere Verbindungen zu meinen GA-Tabellen herstellen muss, kann ich auf die Zellen der Rohdaten verweisen und die benötigten Berichte erstellen. Anschließend visualisiere ich sie mit den Diagrammfunktionen von Google Spreadsheet.


## &#x200B;3. Exporte von Rohdaten

Wenn Sie wirklich Rohdaten benötigen, bieten sowohl Adobe als auch Google die Möglichkeit, Informationen auf diese Weise abzurufen.

### 3.1. Adobe-Daten-Feed

In Abschnitt 2.2.2 habe ich erwähnt, dass die Adobe Analytics-API auf „verarbeitete Daten“ zurückgreift. Der Rohdaten-Feed ruft Daten ab, die durch die im Admin-Bedienfeld festgelegten „Verarbeitungsregeln“ aufbereitet wurden. Aber diese Rohdaten enthalten alle Daten, die sonst überall ausgeschlossen sind.

Das bedeutet, dass alle Ihre Bot-Ausschlüsse, intern gefilterten IP-Daten und anderen ausgeschlossenen Daten in den Rohdaten-Feeds enthalten sind. Es gibt Flags zur Kennzeichnung dieser Daten, sodass Ihr Entwicklungs-Team beim Aufbau eines Data Lake eine Logik zur entsprechenden Verarbeitung dieser Daten erstellen kann.

Die Rohdaten-Feeds können so angepasst werden, dass alle Datenspalten oder nur bestimmte Spalten gesendet werden, wenn Sie einen spezifischeren Feed benötigen.

Die Feeds können direkt an FTP, SFTP oder S3 gesendet werden.


### 3.2. Google Big Query

Leider habe ich mit diesem Google-Tool noch keine Erfahrung, aber theoretisch sollte es ähnlich wie der Daten-Feed von Adobe funktionieren und Ihrem Entwicklungs-Team den Zugriff auf Rohdaten aus Ihrem Google Analytics-Konto ermöglichen.

Statt jedoch einen vollständigen Dump der Rohdaten bereitzustellen, ermöglicht es Ihren Ingenieuren, über SQL-Abfragen auf die Daten zuzugreifen, um gezielte Rohdaten oder alle Spalten der Rohdaten abzurufen.

## &#x200B;4. Schlussfolgerung

Wie bei jedem System ist Übung erforderlich, um sich mit dem Tool vertraut zu machen. Wir hoffen, dieses Handbuch hilft Ihnen bei den ersten Schritten bzw. gibt Ihnen Tipps, wie Sie Adobe Analytics besser nutzen können.

Ich möchte jedoch betonen, dass ich empfehlen würde, sowohl Adobe Analytics als auch Google Analytics in Ihrer Implementierungsstrategie zu verwenden (selbst wenn es nur die kostenlose Version von Google Analytics ist). Auf diese Weise haben Sie auch ein Backup-System, sodass immer Daten verfügbar sind, denn kein System ist unfehlbar.

Neben diesem Handbuch stehen Ihnen viele weitere Ressourcen zur Verfügung, mit denen Sie Ihre Strategie verbessern können:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=de#home) - mit Tutorials, Videos, Dokumentation und Community-Foren
* [Adobe-Benutzergruppen](https://analytics-augs.adobe.com/) – Ein zentraler Treffpunkt für von der Community organisierte Events, die Benutzenden dabei helfen, sich untereinander auszutauschen und ihre Implementierungen zu verbessern.
* [YouTube-Kanal zu Adobe Analytics-Benutzergruppen](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) – Konnten Sie keine Adobe Analytics-Benutzergruppensitzung erstellen? Sehen Sie sich frühere Benutzergruppensitzungen auf der ganzen Welt an, um mehr darüber zu erfahren, wie Ihre Kollegen das Tool verwenden.
* [Measure Chat Slack-Kanal](https://www.measure.chat/) - Treten Sie mit Adobe Analytics-Anwendern in der ganzen Welt in Kontakt und tauschen Sie Branchenkenntnisse aus, stellen Sie Fragen an Ihre Kollegen und schließen Sie sich Interessengruppen an.
* und vieles mehr!

## Autor

Dieses Dokument wurde verfasst von:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, Optimization Manager Analytics bei Torstar

Adobe Analytics-Experte

