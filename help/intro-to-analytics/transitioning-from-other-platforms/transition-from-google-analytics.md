---
title: Umfassender Leitfaden für die Umstellung von Google Analytics auf Adobe Analytics
description: Eine der größten Herausforderungen beim Übergang zwischen verschiedenen Tools besteht darin, zu lernen, wo entsprechende Funktionen zu finden sind und zu lernen, wie sie effizient genutzt werden können. Diese Diskussion ist Teil eines umfassenderen Leitfadens, der Benutzern den Übergang zu Adobe Analytics erleichtert.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830
source-git-commit: 404ec61f8e1ad389f9d0f51d60ce5d9634b0a38c
workflow-type: tm+mt
source-wordcount: '3644'
ht-degree: 1%

---


# Umfassender Leitfaden für die Umstellung von Google Analytics auf Adobe Analytics

## 1. Einleitung

Eine der größten Herausforderungen beim Übergang zwischen verschiedenen Tools besteht darin, zu lernen, wo entsprechende Funktionen zu finden sind und zu lernen, wie sie effizient genutzt werden können. Diese Diskussion ist Teil eines umfassenderen Leitfadens, der Benutzern beim Übergang zu Adobe Analytics hilft (entweder als neuer Benutzer oder als neuer Benutzer von Google Analytics). einen eingehenden Vergleich mit GA; als am ehesten vergleichendes Tool, mit dem die meisten Benutzer vertraut sein werden; wird bereitgestellt, um Benutzern zu helfen, vorhandenes Wissen mit dem neuen Toolset zu korrelieren. Es gibt zwar keinen Ersatz für die Praxis. Dies wird Ihnen helfen, zu beginnen und hoffentlich die Frustrationen zu reduzieren, die Sie während dieser Zeit (oder sogar als Auffrischung nach dem Start in die Swing der Dinge).

Wir sollten auch nur einen kurzen Terminologievergleich durchführen:

| **Beschreibung** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Eine Ereignismetrik, die eine Seite (oder einen Bildschirm in einer App) darstellt, wurde angezeigt | Seitenansicht | Seitenansicht. |
| Eine Metrik, die eine Gruppe von Interaktionen auf Ihrer Website oder in Ihrer App darstellt, die im selben Zeitrahmen stattfinden | Besuch | Sitzung |
| Eine Metrik, die ein identifiziertes Gerät definiert (basierend auf mehreren Kriterien, einschließlich Cookies und anderen Verhaltensmustern zum Zuordnen von Benutzerinformationen) | Unique Visitor | Benutzer |

## 2. Schnittstellen

Eines der Dinge, die ich am häufigsten sehe, wenn Menschen Adobe Analytics und Google Analytics vergleichen, ist, dass Adobe viel passiert - es ist schrecklich für Menschen. Das stimmt, aber es ist auch. sie glauben oder nicht; eine Stärke, keine Schwäche. Adobe bietet eine breite Palette von Tools und Flexibilität bei der Datenvisualisierung, sodass Sie viel mehr Freiheit beim Aufbau Ihrer Anforderungen haben.

Als Erstes betrachten wir die Berichterstellung &quot;vor Ort&quot;.

### 2.1. In-Site-Berichte

#### 2.1.1. Startbildschirm

Sowohl Adobe Analytics als auch Google Analytics bieten eine Möglichkeit, die erste Ansicht anzupassen, die ein Benutzer bei seiner Anmeldung sieht.

##### 2.1.1.1. Arbeitsbereich/Benutzerdefinierter Startbildschirm (Adobe Analytics)

Adobe Analytics geht nicht davon aus, dass ein vordefinierter Bericht erstellt wird, der allen Benutzern bei der Anmeldung angezeigt wird. Die Standard-Startseite führt den Benutzer zum Workspace-Landingscreen, auf dem jeder Benutzer alle Workspace-Berichte anzeigt, die er erstellt oder für ihn freigegeben hat. Außerdem kann jeder Benutzer einen dieser Berichte bei Bedarf als Startbildschirm festlegen.

![image1](assets/ga-to-aa_1.png)

Weitere Informationen zu Workspace finden Sie weiter unten in diesem Handbuch. Siehe Abschnitt 2.1.2.1.

>[!TIP]
>
>Erstellen/teilen Sie einige Standardberichte für Ihre Organisation, sodass diese einen Ausgangspunkt haben, um Informationen anzuzeigen, ohne sofort in die Erstellung eigener Berichte eintauchen zu müssen.



##### 2.1.1.2. Home Screen Insights (Google Analytics)

* Der Google Analytics-Startbildschirm enthält einige vordefinierte Visualisierungen für Sie.  Diese decken Folgendes ab:
* Benutzer, Sitzungen, Absprungrate und Sitzungsdauer in den letzten 7 Tagen
* Benutzer nach Tageszeit in den letzten 30 Tagen
* Aktuelle Benutzer jetzt und Top-aktive Seiten
* Traffic-Kanal, Quelle/Medium und Verweise in den letzten 7 Tagen
* Sitzungen nach Land in den letzten sieben Tagen
* Top-Seiten für die letzten 7 Tage
* Trend aktiver Benutzer für die letzten 30 Tage
* und vieles mehr...

In GA4 haben Benutzer mehr Möglichkeiten, ihre eigenen Berichte anzupassen und zum Startbildschirm hinzuzufügen.

![image2](assets/ga-to-aa_2.png)

Das ist wahrscheinlich das, was Sie am meisten vermissen werden, wenn Sie zur Adobe kommen. Sie verfügen zwar nicht über einen so vordefinierten Startbildschirm, Sie können jedoch einfach einen benutzerdefinierten Arbeitsbereich einrichten, um die oben genannten Anforderungen zu replizieren. Stellen Sie ihn bei Bedarf als Ihren Landingscreen ein. Weitere Informationen hierzu finden Sie später (oder siehe Adobe Workspace in Abschnitt 2.1.2.1).

#### 2.1.2. Report Builder vor Ort

Zusätzlich zu den einfachen Berichten, die von den Analysetools bereitgestellt werden, bietet jedes Tool leistungsfähigere Tools, mit denen Sie Ihre eigenen benutzerspezifischen Berichte erstellen können.

##### 2.1.2.1. Adobe Analytics Workspace

Dies ist der Motor von Adobe Analytics, seit seiner Einführung im Jahr 2017 ist es zum Ausgangspunkt für die Analytics-Analyse geworden und der Hauptgrund, warum der Abschnitt &quot;Berichte&quot;bald veraltet ist.

Mit diesem Tool können Sie Berichte mit nahezu vollständiger Freiheit erstellen.

Der Bericht kann in Bedienfelder unterteilt werden, die eine beliebige Anzahl von Visualisierungen enthalten können. Bedienfelder können auf allgemeine Informationen wie Datumsbereich und allgemeine Segmentfilter festgelegt werden.

Sowohl die Bedienfelder als auch die darin enthaltenen Visualisierungen können in der Größe angepasst und verschoben werden, um Elemente nebeneinander anzuzeigen oder zu gestapeln. Wenn Sie also zwei verschiedene Datensuiten nebeneinander vergleichen möchten, können Sie Bedienfelder erstellen, die 50/50 in der Mitte unterteilen und die beiden Sites nebeneinander darstellen, um einen einfachen Vergleich zu ermöglichen.

Es stehen eine Vielzahl von Visualisierungen zur Verfügung:

* Freiformtabelle
* Kohortentabelle
* Fallout
* Fluss
* Diagramme
   * Bereich (gestapelt und nicht gestapelt)
   * Linie
   * Streuung
   * Balken (gestapelt und nicht gestapelt)
   * Aufzählungszeichen
   * Ringdiagramm
   * Histogramm
   * Horizontalbalken (gestapelt und nicht gestapelt)
* Zuordnung
* Zusammenfassungsblöcke
   * Zusammenfassungsänderung
   * Zusammenfassungstext
   * Text (freies Textfeld zur Eingabe zusätzlicher Informationen für Kontext)
* Venn

Jedes Bedienfeld und jede Visualisierung können einen Titel erhalten und eine Beschreibung darauf angewendet werden, damit der Kontext, der die Informationen anzeigt, besser wiedergegeben wird.
In Adobe gelten Segmente (im Wesentlichen Datenfilter) rückwirkend. Diese können in Spalten Ihrer Freiformtabellen eingefügt werden, um Daten nebeneinander zu vergleichen. Wenn ein Benutzer beispielsweise zwei verschiedene Kategorien auf seiner Site mit Traffic vergleichen möchte; sie könnten ein Segment für &quot;Kategorie A&quot;und ein anderes Segment für &quot;Kategorie B&quot;erstellen.

![image3](assets/ga-to-aa_3.png)

Freiformtabellen ermöglichen nach Bedarf mehrere Spalten und Segmentierungen, um die Daten wie gewünscht zu visualisieren.

Möchten Sie aus den obigen Gründen keine Aufschlüsselung nach Datum anzeigen? Ziehen Sie einfach eine andere Dimension oder ein Segment dorthin, um die Daten anders anzuzeigen ... z. B. Segmente für Gerätetypen zu verwenden, und fügen Sie dann eine Aufschlüsselung nach Betriebssystem für Ihre Mobile-/Tablet-Benutzer hinzu:

![image3](assets/ga-to-aa_4.png)

Workspace ermöglicht es Ihnen, Ihre Kreativität zu nutzen. Sie sind nicht auf &quot;standardmäßige&quot;Aufschlüsselungen beschränkt. Sie können die Visualisierungen erstellen, die Sie benötigen, um sich über die Vergleiche, die Sie ausführen müssen, zu informieren.

>[!TIP]
>
>Scheuen Sie sich nicht zu spielen und zu entdecken, es gibt so viele Möglichkeiten, außerhalb der Box zu denken, sehen, was Sie tun können! Stellen Sie aber auch sicher, dass Sie versuchen zu überprüfen, dass das, was Sie erstellt haben, wirklich zeigt, was Sie denken. Erlebnis hier hilft!

Sie können sogar direkt berechnete Metriken oder Segmente erstellen, die nur im Bericht enthalten sind (verhindern, dass Ihr Segment- und Berechnungsrepository überschwemmt wird). Achten Sie aber auch darauf, fokussierte Elemente zu erstellen, die für bestimmte Berichte benötigt werden, ohne Ihr Unternehmen mit Dingen zu verwechseln, die in anderen Kontexten nicht besonders nützlich sind.

Diese Diskussion ist nur eine Einführung in dieses Tool. Es gibt weitere umfassendere Anleitungen, die Ihnen den Einstieg erleichtern. In diesem Fall können Sie jedoch umfassende Berichte erstellen, z. B.:

![image3](assets/ga-to-aa_5.png)

Beachten Sie auch, dass Arbeitsbereiche nicht automatisch gespeichert werden. So ist es einfacher, einen einmaligen Ad-hoc-Bericht zu erstellen, ohne das Repository Ihres Berichts zu verstopfen.

Eine weitere leistungsstarke Funktion von Arbeitsbereichen ist die Möglichkeit, interaktive Modifikatoren in Form von Dropdown-Menüs auf Ihre Berichte anzuwenden. Diese Dropdown-Listen funktionieren zwar nicht für exportierte CSV- oder PDF-Dateien Ihrer Berichte, ermöglichen es Ihnen jedoch, alle Visualisierungen in einem Bereich im Live-Bericht zu aktualisieren, um unter verschiedenen Bedingungen denselben Bericht anzuzeigen. Es können mehrere Dropdown-Listen verwendet werden. Solange sich die Optionen nicht gegenseitig ausschließen, werden die ausgewählten Elemente stapelweise eingefügt, um eine saubere Darstellung der Informationen zu ermöglichen.

>[!IMPORTANT]
>
>Weitere Informationen zur Verwendung von Dropdown- und Freiformaufschlüsselungen finden Sie unter <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: Dashboards, benutzerdefinierte Berichte und gespeicherte Berichte

Google verfügt über einige Tools zum Erstellen von Berichten auf der Benutzeroberfläche, die jedoch weiterhin den gleichen Anzeigeparametern und Einschränkungen des Berichtabschnitts entsprechen.

Für diejenigen, die in Google Analytics versiert sind, wie Sie das hier lesen, könnten Sie sagen: &quot;Warte mal kurz, was ist mit Google Data Studio, ist das nicht besser mit dem Arbeitsbereich der Adobe?&quot; und Sie hätten Recht, da Data Studio jedoch technisch nicht Teil des Analytics-Tools ist und Verbindungen zu verschiedenen Datenquellen ermöglicht, wird dieses Tool später im Abschnitt &quot;Erweiterter Zugriff auf Berichte&quot;dieser Diskussion behandelt (insbesondere Abschnitt 2.2.3).

Google-Dashboards und benutzerspezifische Berichte ermöglichen es Ihnen, mehrere Visualisierungen in einem Bericht zusammenzuführen. Im Gegensatz zu Workspace sind Sie jedoch weiterhin in einfache Korrelationen eingeschlossen und erfahren, welche Daten in welche Spalten eingefügt werden können.

Eine der größten Herausforderungen bei benutzerspezifischen Berichten besteht darin, dass ein Filter bei der Erstellung für alle Tabs des Berichts gilt... Es gibt keine Möglichkeit, zwei verschiedene Filter innerhalb desselben Berichts zu vergleichen.

Für Oberflächenvergleiche übernimmt sie die Aufgabe. Diese ähneln den Adobe Legacy Dashboards, benutzerdefinierten Berichten und Lesezeichen. Grundlegende Tools zur Unterstützung Ihrer Anforderungen, die sich in der Report Suite befinden.

#### 2.1.3. Berichte

Sowohl Google als auch Adobe verfügen über einige navigierbare Berichte, bei denen es sich um benutzerdefinierte Tabellen und um grundlegende Zeitleistendiagramme handelt, die auf einer Dimension basieren.

##### 2.1.3.1. Adobe Analytics-Berichte

Adobe Analytics verfügt auch über einen Abschnitt &quot;Berichte&quot;, der jedoch größtenteils schrittweise zugunsten der Analysis Workspace eingestellt wird (und für diese Benutzeroberfläche wurde sogar das Ende der Nutzungsdauer angekündigt, da Workspace [Abschnitt 2.1.2.1] ist ein sehr viel leistungsfähigeres Tool), in dem die meisten Tabellen einfacher erstellt und geändert werden können. Die Bereiche der Adobe sind weitaus stärker aufgeschlüsselt, und dies kann entmutigend sein:

![image3](assets/ga-to-aa_6.png)

Da der Zugriff auf die meisten der oben genannten Bereiche über Arbeitsbereiche erfolgt, werde ich einen kurzen Überblick über diese Bereiche und ihre Beziehung zu Google Analytics geben und hier die noch relevanten Berichte hervorheben.

Site-Metriken sind die Erwartungen, die Sie erwarten würden. Sie decken die Standardmetriken ab (Seitenansichten, Unique Visitors, Besuche sowie benutzerspezifische Ereignisse, die Sie eingerichtet haben). Dies ähnelt dem Verhaltensbericht allgemein, enthält jedoch auch einige der Informationen, die Sie in Audience finden würden (da die Adobe die Metriktypen nicht aufteilt).

Hier finden Sie auch &quot;Bot&quot;-Berichte. Der Traffic von Bots wird aus allen Standardberichten ausgeschlossen. Es gibt jedoch zwei Berichte, die Ihnen einen Einblick in die Vorgänge und Bots bieten, die auf Ihre Site gelangen. Dies ist besonders gut, wenn Sie benutzerdefinierte Bot-Regeln einrichten, um bekannte Spammer-Bots auszuschließen, die häufig auf Ihre Site treffen. Sie können Einblicke in die Aktivitäten dieser Bots erhalten, ohne dass Ihre Hauptberichte überflutet werden, aber dieser Traffic. Bot-Berichte sind derzeit nicht über Workspace verfügbar (aber neue Berichtsfunktionen, die in Kürze verfügbar sein werden, ermöglichen es Benutzern, diese Informationen auch dort zu erhalten).

Site-Content ist eine Gruppierung von Adobe-Standarddimensionen: Seitenname, Sitebereiche (Kanäle), Hierarchien (eine Möglichkeit, benutzerdefinierte Drilldown-Berichte zur Organisation innerhalb Ihrer Website zu erstellen), Server (dies ist besonders hilfreich, wenn Sie mehrere Subdomänen auf Ihrer Site haben oder mehrere Sites in einer Tracking Suite taggen) usw. Alle diese sind in Workspace verfügbar.

Mobile ist eine Gruppierung von Mobilgeräte-spezifischen Daten, wie z. B. Geräten, Gerätetypen usw. Alle diese sind in Workspace verfügbar.

Pfade sind ein weiteres dieser Elemente, die in Workspace nicht verfügbar sind ... während Workspace über ein Flussdiagramm verfügt, können Sie die Ein- und Ausgänge nur für eine einzelne Seite/einen einzigen Wert sehen.. während Pfade es Ihnen ermöglichen, die häufigsten Pfade anzuzeigen, die auf Ihrer Website verwendet werden. Standardmäßig ist &quot;Seiten&quot;der erste Pfadbericht, der für Sie eingerichtet ist. Sie können dies jedoch für benutzerdefinierte Eigenschaften aktivieren (z. B. wenn Sie einen Wert vom Typ &quot;Seite&quot;verfolgen würden, könnten Sie sich die Pfade innerhalb von Seitentypen ansehen. Die andere Sache, die ich persönlich über Pfade mag, ist die einfache Art und Weise, wie die Informationen präsentiert werden... Das Flussdiagramm im Arbeitsbereich (je nachdem, wie viel Sie sich anschauen wollen) kann überwältigend werden. Ich empfehle, beide auszuprobieren... sie haben jeweils einen Nutzen und einen Wert, je nachdem, was Sie versuchen zu erreichen. Beachten Sie, dass jede Dimension in &quot;Fluss&quot;verwendet werden kann, während Pfade in einer Eigenschaft im Admin-Bereich eingerichtet werden müssen.

Die Berichte zu Traffic-Quellen, Kampagnen und Marketingkanälen ähneln allesamt dem Akquisebericht in Google. Die Traffic-Quellen konzentrieren sich auf tatsächliche Referrer, Kampagnen, die sich auf Ihre Kampagnencodes konzentrieren, und Marketing-Kanäle konzentrieren sich auch auf Kampagnencodes. Sie wenden jedoch auch zusätzliche Logik an, die von Ihnen für die Verarbeitung der Informationen festgelegt wird. Ich finde, dass die Adobe viel mehr Freiheit bei der Einrichtung Ihrer Regeln bietet, Google eine Menge Dinge für Sie erledigt, und das wird ein wenig Denkwechsel sein. Beachten Sie außerdem, dass die Google-Attribution für Kampagnencodes standardmäßig 6 Monate beträgt und die Adobe standardmäßig auf 1 Woche eingestellt ist. Dies kann in Ihren Admin-Einstellungen geändert werden. In Workspace können Sie jedoch zusätzlich zu jeder Dimension eine benutzerdefinierte Attribution anwenden, wodurch Sie eine wesentlich größere Flexibilität &quot;direkt&quot;erhalten.

Die Berichte Besuchertreue und Besucherprofil ähneln den Zielgruppenberichten in Google Analytics. Die Treue konzentriert sich stärker auf die Rückkehrhäufigkeit, während sich das Besucherprofil mehr auf die Geografie und Technologie der Benutzer konzentriert.

Sowohl benutzerspezifische Konversion als auch benutzerspezifischer Traffic sind benutzerspezifische Dimensionsberichte, Konversionen sind Ihre eVars (wo Sie ein benutzerdefiniertes Ablaufdatum auf den Wert festlegen können - d. h. Treffer, Besuch, Monat, Jahr usw. - und dieser Wert bleibt für diesen Benutzer für die angegebene Zeit erhalten, sofern er nicht überschrieben wird). Traffic-Variablen sind Ihre Eigenschaften, aber Sie können sie auch für Pfadsetzungsberichte oder als Listenelemente einrichten (die mehrere Werte basierend auf einem Trennzeichen Ihrer Wahl aufteilen).

Medien eignen sich für Videos oder Audiodateien, für die Sie ein spezielles Medien-Tracking eingerichtet haben.

Benutzerspezifische Berichte ist ein Abschnitt, in dem Benutzer die Spalten und Aufschlüsselungen anpassen können, die sie in der Berichtsoberfläche erstellt haben, und sie als benutzerspezifischen Bericht speichern können. Da Workspace jedoch, wie oben erwähnt, so leistungsstarke Aufschlüsselungen und Korrelationen ermöglicht, sollten alle angepassten Elemente dort vorgenommen werden. Dies war eine gute Lösung, bevor Workspace existierte.

Der Abschnitt &quot;Lesezeichen&quot;ähnelt dem Abschnitt &quot;Benutzerspezifische Berichte&quot;, in dem häufig verwendete Berichte mit Lesezeichen in der Berichtsoberfläche versehen werden können, damit sie leichter zu finden sind.

Dashboard war ein veraltetes Produkt, mit dem Reportlets von Daten zu einer Visualisierung kombiniert werden konnten. Die Funktionalität in Workspace (Abschnitt 2.1.2.1) ist jedoch so viel einfacher zu verwenden, dass sie nur als Zugriffspunkt für veraltete Berichte existiert, die neu erstellt werden sollten, bevor diese Funktion eingestellt wird.

Ziel ist ein spezieller Berichtsbereich, in dem Personen innerhalb eines bestimmten Zeitraums einen Bericht auf der Grundlage eines Ziels erstellen können, damit Teams Dinge wie Kampagnen überwachen und feststellen können, ob sie auf dem richtigen Weg sind, um ihre Traffic-Ziele zu erreichen.

Alle hier enthaltenen Berichte waren für mehrere Metrikspalten und Dimensionsaufschlüsselungen zulässig. aber die Einfachheit der Visualisierungen und einige der Logik, hinter denen Elemente korreliert werden könnten, könnten manchmal frustrierend sein.

##### 2.1.3.2. Berichte der Google Analytics

Google Analytics unterteilt diese Berichte in die folgenden Abschnitte: Echtzeit, Zielgruppe, Akquise, Verhalten und Konversationen (in GA3) sowie in den Lebenszyklus (mit den Unterabschnitten: Akquise, Interaktion, Monetarisierung, Bindung) und Benutzer (mit den Unterabschnitten: Demografie und Technik).

![image3](assets/ga-to-aa_7.png)

Sie können diese Visualisierungen geringfügig verändern, eine sekundäre Dimensionsaufschlüsselung hinzufügen, die Visualisierung ändern, einen Datenfilter erstellen usw. Sie können Ihre Anpassungen als gespeicherten Bericht speichern.

Diese geben Ihnen schnelle und einfache Einblicke in Ihre Daten. Sie können jedoch Dinge wie Benutzer nicht mit Seitenansichten einer Seite in derselben Tabelle vergleichen und nicht mehr als eine zusätzliche Dimension hinzufügen, um zusätzliche Daten anzuzeigen.

Diese sind gut für schnelle analytische Daten, aber wenn man wirklich tief graben muss, leiden sie unter den Einschränkungen.

### 2.2. Erweiterter Zugriff auf Berichte

Neben der &quot;In-Site-Berichterstellung&quot;bieten die meisten Tools erweiterte Funktionen, mit denen Sie Ihre Analyse außerhalb der Tools durchführen und etwas benutzerspezifischeres erstellen können.

#### 2.2.1. Adobe Analytics Report Builder (Microsoft Excel-Erweiterung)

Workspace ist ein großartiges Tool. Manchmal müssen Sie Ihre Daten jedoch in eine benutzerdefinierte Tabelle übertragen, um mehrere Datenquellen zusammenfügen zu können. Hier kommt Report Builder ins Spiel.

Report Builder ist ein Plug-in für Microsoft Excel, mit dem Sie Verbindungen zu Ihren Adobe Analytics-Daten erstellen können, um Tabellendaten abzurufen, die Sie in Excel bearbeiten können. Um dies effizient zu nutzen, ziehen Sie die Daten in einige Rohdaten-Tabs, verwenden Sie dann Excel-Zellreferenzen, um Daten aus diesen Registerkarten in einen einzigen konsolidierten Bericht zu ziehen, und erstellen Sie dann Diagramme und Visualisierungen.

>[!NOTE]
>
>Report Builder verfügt über eine spezielle Berechtigung, die auf Ihre Benutzer angewendet werden muss, um auf dieses Plug-in zugreifen zu können. Dies sollte wahrscheinlich nur Benutzern gewährt werden, die gelernt haben, das Tool ordnungsgemäß zu verwenden.

#### 2.2.2. Adobe Analytics-API-Verbindung

Wenn Sie möchten, dass Ihr Adobe Analytics von einer anderen Seite als Excel aufgenommen wird, Sie aber dennoch die Vorteile verarbeiteter Daten nutzen möchten (einschließlich der Bot-Regelausschlüsse), können Sie die API der Adobe verwenden, um Daten direkt abzurufen, sie dann über ein Skript zu verarbeiten oder sie einer Datenbank zur Verwendung mit einem anderen System hinzuzufügen.

Beachten Sie, dass die API weiterhin Korrelationsdaten abruft und dabei die Aufschlüsselungen und Segmente anwendet, wie in der Pull-Anforderung angegeben.

Workspace der Adobe (Abschnitt 2.1.2.1) verwendet die API tatsächlich, um alle Berichte zu erstellen. Wenn Sie den Debugmodus in Workspace aktivieren, werden Ihnen die genauen verwendeten API-Aufrufe angezeigt. Auf diese Weise können Sie Ihre API-Aufrufe schnell erstellen, indem Sie Workspace verwenden, um die Daten zu erstellen und zu validieren, die Sie abrufen möchten, und diese API-Aufrufe dann verwenden, um die Daten an Ihre eigene Verarbeitung zu übertragen.


#### 2.2.3. Google Analytics Data Studio

Wenn Sie bereits gelesen haben, wissen Sie bereits von oben, dass ich Data Studio als eine Entsprechung zu Adobe Workspace erwähnt habe. Mit Data Studio können Sie Google Analytics-Daten, aber auch Daten aus anderen Quellen abrufen. Dies ist hilfreich, wenn Sie Ihre Analysedaten mit anderen erfassten Daten konsolidieren möchten. Was jedoch die Google Analytics betrifft, so habe ich die gleichen Visualisierungsbeschränkungen wie bei Google Analytics festgestellt. Die Art und Weise, wie Zeilen und Spalten gebildet werden, ist immer noch sehr begrenzt, was getan werden kann.

Es ist immer noch ein mächtiges Werkzeug, und ich würde die Leute nicht davon abhalten, es in irgendeiner Weise zu verwenden, aber meine persönliche Erfahrung ist, dass, nachdem ich Workspace so lange verwendet habe, ich persönlich das starre Verhalten ziemlich begrenzt finde.


#### 2.2.4. Google Spreadsheet-Erweiterung

Für meine eigenen Zwecke, wenn ich Daten auf erweiterte Weise von Google Analytics abrufen muss, ist mein persönliches Tool die Google-Tabellenkalkulationserweiterung. Natürlich muss ich mehrere Verbindungen zu meinen GA-Tabellen herstellen, aber wie der Report Builder der Adobe kann ich auch auf die Zellen aus den Rohdaten verweisen, die benötigten Berichte erstellen und sie dann mithilfe der Diagrammfunktionen des Google-Arbeitsblatts visualisieren.


## 3. Rohdatenexporte

Für solche Fälle, in denen Sie wirklich Rohdaten benötigen, bieten sowohl Adobe als auch Google die Möglichkeit, Informationen auf diese Weise abzurufen.

### 3.1. Adobe Data Feed

In Abschnitt 2.2.2 erwähnte ich, dass die Adobe Analytics-API aus &quot;verarbeiteten Daten&quot;abgerufen wurde. Der Rohdaten-Feed ruft weiterhin Daten ab, die von den im Admin-Bereich eingerichteten &quot;Verarbeitungsregeln&quot;verarbeitet wurden (stellen Sie sicher, dass Ihre Rohdaten verzögert sind, um sicherzustellen, dass alle diese Regeln zum Zeitpunkt des Abrufs des Rohdaten-Feeds abgeschlossen sind). Diese Rohdaten enthalten jedoch alle Daten, die überall sonst ausgeschlossen sind.

Das bedeutet, dass all Ihre Bot-Ausschlüsse, internen IP-gefilterten Daten usw. in den Rohdaten-Feeds enthalten sind. Es gibt Flags, die diese Daten identifizieren. Wenn Sie also einen Data Lake erstellen, kann Ihr Technikerteam eine Logik zur entsprechenden Verarbeitung dieser Daten erstellen.

Die Rohdaten-Feeds können angepasst werden, um alle Datenspalten oder nur bestimmte Spalten zu senden, wenn Sie einen zielgerichteteren Feed benötigen.

Die Feeds können direkt an FTP, SFTP, S3 usw. gesendet werden.


### 3.2. Google Big Query

Leider habe ich noch keine Erfahrung mit diesem Google-Tool gesammelt. Theoretisch sollte es jedoch dem Daten-Feed der Adobe ähneln, sodass Ihr Technikerteam auf Rohdaten aus Ihrem Google Analytics-Konto zugreifen kann.

Ich glaube jedoch, dass es Ihren Ingenieuren nicht nur erlaubt, auf die Daten mittels SQL-Abfragen zuzugreifen, sondern sie können entweder zielgerichtete Rohdaten abrufen oder, wenn sie möchten, alle Spalten von Rohdaten abrufen, um sie in einen Data Lake aufzunehmen.

## 4. Schlussfolgerung

Wie bei jedem System ist Übung erforderlich, um sich damit vertraut zu machen, aber hoffentlich wird dieser Leitfaden Sie zu den ersten Schritten bringen oder Ihnen Tipps geben, um Ihre Nutzung von Adobe Analytics zu verbessern, wenn Sie nur die Oberfläche gekratzt haben.

Ich möchte jedoch betonen, dass ich empfehlen würde, sowohl Adobe Analytics als auch Google Analytics in Ihrer Implementierungsstrategie zu verwenden (auch wenn die Google Analytics nur die freie Version sind). Dadurch können Sie über ein Backup-System verfügen, um sicherzustellen, dass Sie über Daten verfügen, da kein System unfehlbar ist.

Neben diesem Handbuch stehen Ihnen viele Ressourcen zur Verfügung, die Ihnen helfen, Ihre Strategie zu verbessern:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=de#home) (enthält Tutorials, Videos, Dokumentation und Community-Foren)
* [Adobe-Benutzergruppen](https://analytics-augs.adobe.com/) (Dies ist ein Knotenpunkt von Community-Ausführungsereignissen, die Benutzern dabei helfen, miteinander zu kommunizieren und ihre Implementierungen zu verbessern - nur weil diese in einer bestimmten Zeitzone basieren, ist es am besten zu überprüfen, welche anderen Regionen ebenfalls ausgeführt werden.)
* YouTube-Kanal
   * [Adobe Analytics-Benutzergruppen](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA)
* Slack-Kanäle
   * [Chat messen](https://www.measure.chat/)
* und vieles mehr...

## Autor

Dieses Dokument wurde geschrieben von:

![Jennifer Dugan](assets/Jennifer_Dungan_Headshot150.png)

Adobe Analytics Champion

Jennifer Dugan, Optimization Manager Analytics bei Torstar
