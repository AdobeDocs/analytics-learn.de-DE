---
title: Umfassendes Handbuch für die Umstellung von Google Analytics auf Adobe Analytics
description: Erfahren Sie mehr über die Position äquivalenter Funktionen und wie Sie sie beim Übergang von Google Analytics zu Adobe Analytics effizient verwenden können.
feature: Third-party Integration
role: User
level: Beginner
kt: 9830
thumbnail: 34749.jpg
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '3380'
ht-degree: 48%

---

# Umfassendes Handbuch für die Umstellung von Google Analytics auf Adobe Analytics{#comprehensive-guide-for-transitioning-to-Adobe-Analytics}

## 1. Einführung

Eine der größten Herausforderungen bei der Umstellung von einem Tool auf ein anderes besteht darin, zu lernen, wo die entsprechenden Funktionen zu finden sind und wie man sie effizient nutzt. Diese Ausführungen sind Teil einer umfangreicheren Anleitung, die Benutzern den Umstieg auf Adobe Analytics erleichtern soll (entweder als neuer Benutzer oder als jemand, der zuvor Google Analytics verwendet hat). einen eingehenden Vergleich mit GA; als das am ehesten vergleichende Tool, mit dem die meisten Benutzer vertraut sind; wird bereitgestellt, um Benutzern zu helfen, vorhandenes Wissen mit dem neuen Toolset zu korrelieren. Wenn es keinen Ersatz für Übung gibt, hilft dies Ihnen, zu beginnen und Frustrationen zu reduzieren, die während dieser Zeit auftreten können.

Wir sollten einen schnellen Terminologievergleich durchführen:

| **Beschreibung** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Eine Ereignismetrik, die anzeigt, dass eine Seite (oder ein Bildschirm in einer Mobile App) angesehen wurde | Seitenansicht | Seitenansicht. |
| Eine Metrik, die eine Reihe von Interaktionen auf Ihrer Website oder Mobile App darstellt, welche im gleichen Zeitrahmen stattfinden | Besuch | Sitzung |
| Eine Metrik, die ein identifiziertes Gerät definiert (basierend auf mehreren Kriterien, einschließlich Cookies und anderen Verhaltensmustern, um Benutzerinformationen zu vereinen) | Unique Visitor | Benutzer |

## 2. Die Benutzeroberfläche

Wenn Menschen Adobe Analytics und Google Analytics vergleichen, kommentieren sie, dass die Benutzeroberfläche der Adobe anfangs erschreckend ist. Das stimmt, es ist aber – ob Sie es glauben oder nicht – eine Stärke und keine Schwäche. Adobe bietet eine breite Palette von Werkzeugen und große Flexibilität bei der Datenvisualisierung, sodass Sie viel mehr Freiheit in der visuellen Darstellung haben.

Beginnen wir mit dem „In-Site“-Reporting.

### 2.1. In-Site-Reporting

#### 2.1.1. Startbildschirm

Sowohl Adobe Analytics als auch Google Analytics bieten die Möglichkeit, die erste Ansicht, die ein Benutzer bei der Anmeldung sieht, anzupassen.

##### 2.1.1.1. Workspace / Benutzerdefinierter Startbildschirm (Adobe Analytics)

Adobe Analytics erstellt keinen vorgefertigten Bericht, der allen Benutzern bei der Anmeldung präsentiert wird. Die Standard-Startseite führt den Benutzer zum Workspace-Landingscreen, auf dem jeder Benutzer alle Workspace-Berichte anzeigt, die er erstellt oder für ihn freigegeben hat. Außerdem kann jeder Benutzer einen dieser Berichte auf seinem Startbildschirm einrichten, sofern er dies wünscht.

![workspace-create-project](assets/ga-to-aa_1.png)

Weitere Informationen zu Workspace finden Sie weiter unten in diesem Handbuch. Siehe Abschnitt 2.1.2.1

>[!TIP]
>
>Erstellen/Teilen Sie einige Standardberichte für Ihre Organisation, damit die Benutzer einen Ausgangspunkt haben, um Informationen zu sehen, ohne gleich ihre eigenen Berichte erstellen zu müssen.



##### 2.1.1.2. Startbildschirm-Insights (Google Analytics)

* Der Google Analytics-Startbildschirm bietet Ihnen einige vordefinierte Visualisierungen. Diese umfassen u. a. Folgendes:
* Benutzer, Sitzungen, Absprungrate und Sitzungsdauer in den letzten sieben Tagen
* Benutzer nach Tageszeit in den letzten 30 Tagen
* Aktuelle Benutzer und die aktivsten Seiten
* Traffic-Kanal, Quelle/Medium und Verweise in den letzten sieben Tagen
* Sitzungen nach Land in den letzten sieben Tagen
* Top-Seiten für die letzten sieben Tage
* Trend der aktiven Benutzer für die letzten 30 Tage
* und vieles mehr

GA4 haben die Benutzer mehr Möglichkeiten, den Startbildschirm anzupassen und ihre eigenen Berichte hinzuzufügen.

![google-analytics-interfaces](assets/ga-to-aa_2.png)

Das ist wahrscheinlich das eine, was Sie in Adobe Analytics am meisten vermissen. Es ist kein Startbildschirm für Sie vorkonfiguriert. Sie können jedoch einfach einen benutzerdefinierten Arbeitsbereich einrichten, um das, was Sie benötigen, aus der obigen Liste zu replizieren und es als Ihren Landingscreen festzulegen. Weitere Informationen zu diesem Thema finden Sie später (oder siehe Abschnitt 2.1.2.1 Adobe Workspace).

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

Wenn Sie keine Aufschlüsselung nach Datum sehen möchten, ziehen Sie einfach eine andere Dimension oder ein Segment dorthin, um die Daten auf eine andere Weise anzuzeigen. Verwenden Sie beispielsweise Segmente für Gerätetyp und fügen Sie dann eine Aufschlüsselung nach Betriebssystem für Ihre Mobile-/Tablet-Benutzer hinzu:

![analytics-compare-page-views-report](assets/ga-to-aa_4.png)

Mit Workspace können Sie Ihrer Kreativität freien Lauf lassen, Sie sind nicht auf Standard-Aufschlüsselungen beschränkt. Sie können die Visualisierungen erstellen, die Sie benötigen, um aufschlussreiche Vergleiche auszuführen.

>[!TIP]
>
>Hab keine Angst zu spielen und zu erforschen. Es gibt so viele Möglichkeiten, außerhalb der Kiste zu denken. Überprüfen Sie außerdem, was Sie erstellt haben, indem Sie anzeigen, was Sie denken. Erfahrung hilft!

Sie können direkt berechnete Metriken oder Segmente erstellen, die nur im Bericht enthalten sind, um zu verhindern, dass Ihr Segment- und Berechnungsrepository überschwemmt wird. Auf diese Weise können Sie fokussierte Elemente erstellen, die für bestimmte Berichte benötigt werden, ohne Ihr Unternehmen mit Elementen zu verwechseln, die in anderen Kontexten nicht verwendet werden können.

Diese Diskussion ist nur eine Einführung in dieses Tool, es gibt weitere umfassende Anleitungen, um Ihnen den Einstieg zu erleichtern. Nachdem Sie diese Handbücher überprüft haben, erstellen Sie umfassende Berichte wie die folgenden:

![workspace-dashboard](assets/ga-to-aa_5.png)

Arbeitsbereiche werden nicht automatisch gespeichert. So ist es einfacher, einen einmaligen Ad-hoc-Bericht zu erstellen, ohne das Repository Ihres Berichts zu verstopfen.

Ein weiteres leistungsstarkes Merkmal von Arbeitsbereichen ist die Möglichkeit, interaktive Modifikatoren in Form von Dropdown-Menüs auf Ihre Berichte anzuwenden. Diese Dropdown-Listen funktionieren nicht mit exportierten CSV- oder PDF-Dateien Ihrer Berichte. Im Live-Bericht können Sie jedoch alle Visualisierungen in einem Bedienfeld aktualisieren, um denselben Bericht unter verschiedenen Bedingungen anzuzeigen. Es können mehrere Dropdown-Listen verwendet werden. Sofern sich die Optionen nicht gegenseitig ausschließen, werden die ausgewählten Elemente stapelweise eingefügt, um eine saubere Darstellung der Informationen zu ermöglichen.

>[!IMPORTANT]
>
>Weitere Informationen über die Verwendung von Dropdown-Menüs und Freiform-Aufgliederungen finden Sie unter <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: Dashboards, benutzerdefinierte Berichte und gespeicherte Berichte

Google verfügt über einige Tools zur Erstellung von Berichten innerhalb der Benutzeroberfläche, die jedoch die gleiche Darstellung und die gleichen Einschränkungen wie der Bereich mit den Berichten aufweisen.

Wer sich mit Google Analytics auskennt, wird sich jetzt vielleicht fragen, ob Google Data Studio nicht ein besseres Äquivalent zu Adobes Workspace ist. Ja, aber Data Studio ist technisch nicht Teil des Analytics-Tools und ermöglicht Verbindungen zu verschiedenen Datenquellen. Dieses Tool wird später im Abschnitt &quot;Erweiterter Zugriff auf Berichte&quot;behandelt, insbesondere Abschnitt 2.2.3.

Google-Dashboards und benutzerdefinierte Berichte ermöglichen es Ihnen, mehrere Visualisierungen in einem Bericht zusammenzufassen. Im Gegensatz zu Workspace sind Sie aber immer noch auf einfache Korrelationen beschränkt und können nicht festlegen, welche Daten in welche Spalten eingefügt werden können.

Eine der größten Herausforderungen in benutzerspezifischen Berichten besteht darin, einen Filter zu erstellen. Dieser gilt für alle Tabs des Berichts. Es gibt keine Möglichkeit, zwei verschiedene Filter im selben Bericht zu vergleichen.

Bei Oberflächenvergleichen wird der Vorgang ausgeführt. Diese ähneln den alten Dashboards, benutzerspezifischen Berichten und Lesezeichen der Adobe. Grundlegende Tools zur Erfüllung Ihrer Anforderungen, die in der Report Suite enthalten sind.

#### 2.1.3. Berichte

Sowohl Google als auch Adobe verfügen über einige navigierbare Berichte, bei denen es sich um vorgefertigte Tabellen und einfache Zeitreihendiagramme handelt, die auf einer Dimension basieren.

##### 2.1.3.1. Adobe Analytics-Berichte

Adobe Analytics verfügt auch über einen Abschnitt &quot;Berichte&quot;, der jedoch schrittweise zugunsten von Analysis Workspace eingestellt wird. Tatsächlich wurde das Ende des Lebenszyklus für diese Benutzeroberfläche angekündigt, da Workspace ein leistungsfähigeres Tool ist. Die meisten dieser Tabellen können einfacher erstellt und geändert werden. Bei Adobe sind die Abschnitte viel stärker untergliedert, was entmutigend wirken kann:

![analytics-site-metrics](assets/ga-to-aa_6.png)

Da der Zugriff auf die meisten der oben genannten Bereiche über Arbeitsbereiche erfolgt, gebe ich einen kurzen Überblick über diese Bereiche und ihre Beziehung zu Google Analytics und möchte die noch relevanten Berichte hier hervorheben.

Site-Metriken sind die Erwartungen, die Sie erwarten würden. Sie decken die Standardmetriken ab (Seitenansichten, Unique Visitors, Besuche und benutzerspezifische Ereignisse, die Sie eingerichtet haben). Dieser Bericht ähnelt dem Verhaltensbericht in GA, enthält aber auch einige der Informationen, die Sie unter „Zielgruppe“ finden würden (da Adobe die verschiedenen Metriktypen nicht aufteilt).

Hier finden Sie &quot;Bot&quot;-Berichte. Traffic von Bots wird aus allen Standardberichten ausgeschlossen. Es gibt jedoch zwei Berichte, die Aufschluss darüber geben, was passiert und welche Bots zu Ihrer Site gelangen. Dies ist besonders nützlich, wenn Sie benutzerdefinierte Bot-Regeln eingerichtet haben, um bekannte Spam-Bots auszuschließen, die häufig Ihre Website besuchen. So erhalten Sie einen Einblick in die Aktivitäten dieser Bots, ohne dass Ihre Hauptberichte mit deren Traffic überflutet werden. Bot-Berichte sind derzeit nicht über Workspace verfügbar (aber neue Berichtsfunktionen, die in Kürze verfügbar sind, ermöglichen es Benutzern, diese Informationen auch dort zu erhalten).

Site-Content ist eine Gruppierung von Adobe-Standarddimensionen: Seitenname, Sitebereiche, Hierarchien, Server und mehr. Alle diese Dimensionen sind in Workspace verfügbar.

Mobile ist eine Gruppierung mobilgerätespezifischer Daten, einschließlich Geräten, Gerätetypen und mehr. Diese sind in Workspace verfügbar.

Pfade sind in Workspace nicht verfügbar. Workspace verfügt über ein Flussdiagramm, in dem Sie die Ein- und Aus-Flüsse für eine einzelne Seite/einen einzelnen Wert sehen können. Im Gegensatz dazu können Sie mit Pfaden die gängigsten Pfade sehen, die auf Ihrer Website verwendet werden. Standardmäßig ist &quot;Seiten&quot;der erste Pfadbericht, der für Sie eingerichtet wurde. Sie können dies jedoch für benutzerdefinierte Eigenschaften wie den Wert &quot;Seitentyp&quot;aktivieren. Sie können sich die Pfade innerhalb von Seitentypen ansehen. Ein weiterer Punkt, der mir persönlich an der Funktion „Pfade“ gefällt, ist die einfache Art und Weise, in der die Informationen präsentiert werden... Das Flussdiagramm in Workspace kann (abhängig von der angezeigten Datenmenge) schnell überwältigend werden. Ich empfehle, beide auszuprobieren... beide haben ihren Nutzen und Wert, je nachdem, was Sie erreichen wollen. Es sollte beachtet werden, dass für „Flüsse“ jede Dimension verwendet werden kann, während die Pfadbestimmung in einer Prop in der Verwaltungskonsole eingerichtet werden muss.

Die Berichte zu Traffic-Quellen, Kampagnen und Marketingkanälen ähneln dem Akquisebericht des Google-Produkts. Der Bericht über Traffic-Quellen konzentriert sich auf die tatsächlichen Referrer, der Bericht über Kampagnen konzentriert sich auf Ihre Kampagnen-Codes und der Bericht über Marketing-Kanäle konzentriert sich ebenfalls auf Kampagnen-Codes, wendet aber zusätzlich eine von Ihnen festgelegte Logik an, wie die Informationen zu verarbeiten sind. Adobe bietet mehr Freiheit beim Einrichten von Regeln. Im Gegensatz dazu macht Google viele Dinge für Sie, und das ist ein Denkwechsel. Standardmäßig beträgt die Attribution von Google für Campaign-Codes sechs Monate. Die Attribution der Adobe ist standardmäßig auf eine Woche eingestellt. Sie können dies zwar in Ihren Admin-Einstellungen ändern, aber in Workspace können Sie tatsächlich eine benutzerdefinierte Attribution auf jede Dimension anwenden, was Ihnen viel mehr spontanen Spielraum bietet.

Die Berichte zur Besucherbindung und zum Besucherprofil ähneln den Zielgruppenberichten in Google Analytics. Die Besucherbindung konzentriert sich eher auf die Häufigkeit der Wiederkehr, während das Besucherprofil eher auf die Geografie und Technologie der Nutzer ausgerichtet ist.

Benutzerspezifische Konversions- und benutzerspezifische Traffic-Berichte sind beide benutzerspezifische Dimensionsberichte. Konversionen sind eVars. Sie können für einen benutzerdefinierten Ablauf den Wert festlegen, z. B. Treffer, Besuch, Monat und Jahr. Dieser Wert bleibt für einen Benutzer für den konfigurierten Zeitraum persistent, es sei denn, er wurde überschrieben. Traffic-Variablen sind Props. Sie können diese auch für Pfadsetzungsberichte oder als Listenelemente einrichten, die mehrere Werte basierend auf einem Trennzeichen Ihrer Wahl aufteilen.

„Medien“ ist z. B. für Videos oder Audiodateien, für die Sie ein spezielles Medien-Tracking eingerichtet haben.

„Benutzerdefinierte Berichte“ ist ein Bereich, in dem ein Benutzer die Spalten und Aufschlüsselungen, die er innerhalb der Berichtsschnittstelle erstellt hat, anpassen und als benutzerdefinierten Bericht speichern kann. Da Workspace jedoch, wie oben erwähnt, so leistungsstarke Aufschlüsselungen und Korrelationen ermöglicht, sollten alle angepassten Elemente dort vorgenommen werden. Dies war eine gute Lösung, bevor es Workspace gab.

Der Abschnitt „Lesezeichen“ ähnelt den benutzerdefinierten Berichten, wo häufig verwendete Berichte in der Berichtsschnittstelle mit Lesezeichen versehen werden können, damit sie leichter gefunden werden können.

Dashboard war ein älteres Produkt, das es ermöglichte, Reportlets von Daten in einer Visualisierung zu kombinieren. Die Funktionalität in Workspace (Abschnitt 2.1.2.1) ist jedoch so viel einfacher zu handhaben, dass es nur noch als Zugangspunkt zu alten Berichten existiert, die neu erstellt werden sollten, bevor diese Funktion eingestellt wird.

Mit Zielgruppen können Benutzer innerhalb eines bestimmten Zeitraums einen Bericht erstellen, der auf einem Ziel basiert. Teams überwachen Kampagnen, um festzustellen, ob sie auf dem richtigen Weg sind, um ihre Traffic-Ziele zu erreichen.

Alle Berichte in diesem Bereich können nach mehreren metrischen Spalten und Dimensionen aufgeschlüsselt werden. Die Einfachheit der Visualisierungen und einige der Logik, hinter denen Elemente korreliert werden können, könnten jedoch manchmal frustrierend sein.

##### 2.1.3.2. Google Analytics-Berichte

Google Analytics unterteilt diese Berichte in die folgenden Abschnitte: Realtime, Audience, Acquisition, Behavior und Conversations (in GA3) sowie in den Lebenszyklus (mit den Unterabschnitten: Akquise, Interaktion, Monetarisierung, Bindung) und Benutzer (mit den Unterabschnitten: Demografie und Technik).

![google-analytics-interface-compare](assets/ga-to-aa_7.png)

Sie können kleinere Änderungen an diesen Visualisierungen vornehmen, eine sekundäre Dimensionsaufschlüsselung hinzufügen, die Visualisierung ändern, einen Filter für die Daten erstellen und vieles mehr. Sie können Ihre Anpassungen als gespeicherten Bericht speichern.

Diese bieten schnelle und einfache Einblicke in Ihre Daten. Sie können jedoch nicht Dinge wie Benutzer mit Seitenaufrufen für eine Seite in derselben Tabelle vergleichen und Sie können nicht mehr als eine zusätzliche Dimension hinzufügen, um zusätzliche Daten zu sehen.

Diese Berichte eignen sich gut für die schnelle Analyse von Daten, aber wenn Sie wirklich in die Tiefe gehen müssen, stellen diese Einschränkungen ein Problem dar.

### 2.2. Erweiterter Zugriff auf Berichte

Neben der &quot;In-Site-Berichterstellung&quot;bieten die meisten Tools erweiterte Funktionen, mit denen Sie Ihre Analyse außerhalb der Tools durchführen und etwas kundenspezifischer erstellen können.

#### 2.2.1. Adobe Analytics Report Builder (Microsoft® Excel-Erweiterung)

Workspace ist ein großartiges Tool, aber manchmal müssen Sie Ihre Daten in eine benutzerdefinierte Kalkulationstabelle übertragen, möglicherweise mit dem Ziel, mehrere Datenquellen miteinander zu verknüpfen. An dieser Stelle kommt Report Builder ins Spiel.

Report Builder ist ein Plug-in für Microsoft® Excel, mit dem Sie Verbindungen zu Ihren Adobe Analytics-Daten erstellen können, um Tabellendaten abzurufen, die Sie in Excel bearbeiten können. Um dies effizient zu nutzen, würden Sie in der Regel die Daten in einige Rohdaten-Registerkarten einlesen und dann Zellverweise in Excel verwenden, um die Daten aus diesen Registerkarten in einen einzigen konsolidierten Bericht einzulesen und dann Diagramme und Visualisierungen zu erstellen.

>[!NOTE]
>
>Report Builder verfügt über eine spezielle Zugriffsberechtigung, die auf Ihre Benutzer angewendet werden muss, damit sie auf dieses Plug-in zugreifen können. Dies sollte Benutzern gewährt werden, die gelernt haben, das Tool ordnungsgemäß zu verwenden.

#### 2.2.2. Adobe Analytics-API-Verbindung

Wenn Sie Adobe Analytics-Daten benötigen, die von einer anderen als Excel-Datei aufgenommen werden sollen, und die verarbeiteten Daten einschließlich der Bot-Regelausschlüsse erhalten sollen, verwenden Sie die API der Adobe, um die Daten direkt abzurufen. Verarbeiten Sie dann die Daten mithilfe eines Skripts oder fügen Sie sie einer Datenbank hinzu, um sie mit einem anderen System zu verwenden.

Es sollte beachtet werden, dass die API nach wie vor Korrelationsdaten abruft, wobei die in der Abrufanfrage angegebenen Aufschlüsselungen und Segmente angewendet werden.

Der Arbeitsbereich von Adobe (Abschnitt 2.1.2.1) verwendet die API zum Erstellen der Berichte. Wenn Sie den Debug-Modus in Workspace aktivieren, werden die genauen verwendeten API-Aufrufe angezeigt. Auf diese Weise können Sie Ihre API-Aufrufe schnell erstellen. Indem Sie Workspace zum Erstellen und Überprüfen der Daten verwenden, die Sie abrufen möchten, verwenden Sie diese API-Aufrufe, um die Daten an Ihre eigene Verarbeitung zu übertragen.


#### 2.2.3. Google Analytics Data Studio

Wenn Sie schon gelesen haben, wissen Sie bereits von oben, dass ich Data Studio als eine Entsprechung zu Adobe Workspace erwähnt habe. Mit Data Studio können Sie Google Analytics-Daten, aber auch Daten aus anderen Quellen einlesen. Dies ist hilfreich, wenn Sie Ihre Analysedaten mit anderen erfassten Daten zusammenführen möchten. Bei Google Analytics gibt es jedoch dieselben Visualisierungsbeschränkungen. Die Form der Zeilen und Spalten ist weiterhin eingeschränkt.

Es ist immer noch ein mächtiges Werkzeug, und ich würde die Leute nicht davon abhalten, es in irgendeiner Weise zu verwenden. Meine persönliche Erfahrung ist, dass ich das starre Verhalten ziemlich begrenzt finde.


#### 2.2.4. Google Tabellen-Erweiterung

Für meine eigenen Zwecke, wenn ich erweiterte Daten von Google Analytics abrufen muss, ist mein persönliches Tool der Wahl die Google Tabellen-Erweiterung. Obwohl ich mehrere Verbindungen zu meinen GA-Tabellen herstellen muss, kann ich die Zellen aus den Rohdaten referenzieren und die benötigten Berichte erstellen. Dann visualisieren Sie sie mit den Diagrammfunktionen des Google-Arbeitsblatts.


## 3. Exporte von Rohdaten

Wenn Sie Rohdaten wirklich benötigen, bieten sowohl Adobe als auch Google die Möglichkeit, Informationen auf diese Weise abzurufen.

### 3.1. Adobe-Daten-Feed

In Abschnitt 2.2.2 habe ich erwähnt, dass die Adobe Analytics-API auf „verarbeitete Daten“ zurückgreift. Der Rohdaten-Feed ruft Daten ab, die von den &quot;Verarbeitungsregeln&quot;verarbeitet werden, die im Admin-Bereich eingerichtet wurden. Diese Rohdaten enthalten jedoch alle Daten, die überall sonst ausgeschlossen sind.

Das bedeutet, dass sich all Ihre Bot-Ausschlüsse, internen IP-gefilterten Daten und anderen ausgeschlossenen Daten in den Rohdaten-Feeds befinden. Es gibt Flags, die diese Daten identifizieren. Wenn Sie also einen Data Lake erstellen, kann das Technikerteam eine Logik erstellen, um diese Daten entsprechend zu verarbeiten.

Die Rohdaten-Feeds können so angepasst werden, dass alle Datenspalten oder nur bestimmte Spalten gesendet werden, wenn Sie einen spezifischeren Feed benötigen.

Die Feeds können direkt an FTP, SFTP oder S3 gesendet werden.


### 3.2. Google Big Query

Leider ist dies ein Google-Tool, mit dem ich keine Erfahrung gemacht habe. Theoretisch sollte sie dem Daten-Feed von Adobe ähneln, sodass Ihr Technikerteam auf Rohdaten aus Ihrem Google Analytics-Konto zugreifen kann.

Anstatt jedoch eine vollständige Ablage von Rohdaten bereitzustellen, können Ihre Ingenieure über SQL-Abfragen auf die Daten zugreifen, um gezielte Rohdaten oder alle Spalten von Rohdaten abzurufen.

## 4. Schlussfolgerung

Wie jedes System ist Übung erforderlich, um sich mit dem Werkzeug vertraut zu machen. Hoffentlich hilft Ihnen dieses Handbuch bei den ersten Schritten oder bietet Tipps zur Verbesserung Ihrer Nutzung von Adobe Analytics.

Ich möchte jedoch betonen, dass ich empfehlen würde, sowohl Adobe Analytics als auch Google Analytics in Ihrer Implementierungsstrategie zu verwenden (selbst wenn es nur die kostenlose Version von Google Analytics ist). Auf diese Weise haben Sie auch ein Backup-System, sodass immer Daten verfügbar sind, denn kein System ist unfehlbar.

Neben diesem Handbuch stehen Ihnen viele weitere Ressourcen zur Verfügung, mit denen Sie Ihre Strategie verbessern können:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=de#home) - mit Tutorials, Videos, Dokumentation und Community-Foren
* [Adobe-Benutzergruppen](https://analytics-augs.adobe.com/) - Eine zentrale Anlaufstelle für von der Community geleitete Ereignisse, die Benutzern dabei helfen, miteinander zu kommunizieren und ihre Implementierungen zu verbessern.
* [Adobe Analytics-Benutzergruppen YouTube-Kanal](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - Konnte keine Adobe Analytics-Benutzergruppensitzung durchführen? Sehen Sie sich frühere Benutzergruppensitzungen auf der ganzen Welt an, um mehr darüber zu erfahren, wie Ihre Kollegen das Tool verwenden.
* [Measure Chat Slack-Kanal](https://www.measure.chat/) - Treten Sie mit Adobe Analytics-Anwendern in der ganzen Welt in Kontakt und tauschen Sie Branchenkenntnisse aus, stellen Sie Fragen an Ihre Kollegen und schließen Sie sich Interessengruppen an.
* und vieles mehr!

## Autor

Dieses Dokument wurde verfasst von:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, Optimization Manager Analytics bei Torstar

Adobe Analytics-Experte

