---
title: Unterschiede zwischen Segment Builder und Schnellsegmenten in Analysis Workspace
description: Segmente können eines der leistungsfähigsten Tools in Ihrem Toolkit für die Datenanalyse sein. Lernen Sie die Unterschiede zwischen der Verwendung des Segment Builders und Schnellsegmenten in Analysis Workspace kennen, um Effizienz zu erzielen.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
source-git-commit: 9484b2e981d78be59b6ea16eeae2cf6f212c81ab
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 1%

---


# Unterschiede zwischen Segment Builder und Schnellsegmenten in Analysis Workspace

Segmente können eines der leistungsfähigsten Tools in Ihrem Toolkit für die Datenanalyse sein. Lernen Sie die Unterschiede zwischen der Verwendung des Segment Builders und Schnellsegmenten in Analysis Workspace kennen, um Effizienz zu erzielen.

>[!TIP]
>
> Klicken Sie unten auf der Seite auf das Bild, um eine hilfreiche Erinnerung dazu herunterzuladen, wann die einzelnen Tools in Analysis Workspace verwendet werden sollen.

Segmente können eines der leistungsfähigsten Tools in Ihrem Toolkit für die Datenanalyse sein. Wenn Sie bestimmte Traffic-Gruppen, Sitebereiche oder Journey betrachten möchten, können Sie die Segmentierung als eine gute Möglichkeit nutzen, Ihre Analyse auf eine bestimmte Untergruppe von Traffic auf Ihrer Site zu konzentrieren. Aus einer Einzelhandelsumgebung stammen einige der nützlichsten Segmente, die ich erstellt habe, aus verschiedenen Kundengruppen, z. B. neuen oder vorhandenen Kunden, Kunden, die sich bei einem Konto angemeldet haben, gegenüber Gästen usw. Sie können sie aber auch für verschiedene Sitebereiche, Kunden, die bestimmte Aktionen durchführen, oder für alles andere erstellen, woran Sie denken können!

**Es gibt zwei Möglichkeiten zum Erstellen von Segmenten:**

* Verwenden des Segment Builders im Menü &quot;Komponenten&quot;
* Verwenden der Schnellsegmente oben in einem Bedienfeld

Wenn Sie Ihr Segment mit Segment Builder erstellen, können Sie es speichern, um es in anderen Projekten wiederzuverwenden. Dies ist eine hervorragende Möglichkeit, um sich auf bestimmte Gruppen von Kunden zu konzentrieren, z. B. Personen, die bestimmte Bereiche der Site besuchen und dann einen Kauf tätigen. Wenn Sie hingegen eine Sondierungsanalyse durchführen und verschiedene Segmenteinstellungen testen möchten, kann der schnelle Segment-Builder eine große Hilfe sein. Sehen wir uns einige der wichtigsten Vorteile jeder Methode an.

## Schnellsegmente

Am oberen Rand jedes Bedienfelds können Sie auf das Schnellsegmentsymbol (ein Trichter mit dem Symbol + ) klicken, um den Builder zu öffnen. Auf diese Weise können Sie ein Segment auf jeder Ebene (Treffer, Besuch oder Besucher) mit bis zu drei Bedingungen erstellen. Ähnlich wie der Segment Builder gibt Ihnen dies auf der rechten Seite einen Hinweis dazu, dass Hinweise angezeigt werden, ob das Segment Daten zurückgibt und % der gesamten Traffic-Population im Segment enthalten ist. Dies ist jedoch eine vereinfachtere Version als die vollständige Ansicht des Segmentvolumens, die im Segment Builder angezeigt wird. Wenn Sie mehr als eine Bedingung hinzufügen, können Sie die Operatoren &quot;und&quot;und &quot;oder&quot;verwenden. Leider gibt es keine &quot;Dann&quot;-Option für schnelle Segmente. Wenn Sie also sequenzielle Segmente benötigen, müssen Sie den vollständigen Segment-Builder verwenden. Ein Container in einem Schnellsegment ist ebenfalls begrenzt. Da es wirklich für grundlegende Segmente verwendet werden soll, die schnell erstellt und bearbeitet werden können. Sobald ein schnelles Segment auf ein Bedienfeld angewendet oder gespeichert wurde, kann es nicht mehr im Bedienfeld bearbeitet werden.

Wenn Sie eine explorative Analyse durchführen und verschiedene Segmenttypen testen möchten, um zu sehen, wie verschiedene Kundengruppen reagieren oder wie verschiedene Kategorien funktionieren - die Verwendung von schnellen Segmenten ist viel schneller als die Verwendung des Segment Builders. Darüber hinaus sind diese Segmente nur in dem Projekt verfügbar, in dem sie erstellt wurden. Wenn sich also herausstellt, dass sie nicht die gewünschten Ergebnisse liefern, müssen Sie sich nicht darum kümmern, das gespeicherte Segment aus der Übergeordneten Liste zu löschen. Wenn Sie nach dem Testen der Segmente feststellen, dass dies in anderen Projekten nützlich sein wird, können Sie jederzeit auf die Schaltfläche &quot;Builder öffnen&quot;klicken, um das Segment im vollständigen Segment-Builder zu öffnen und es als normales Segment zu speichern. Danach können Sie sie jedoch nicht mehr im Quick Segment Builder bearbeiten.

![Schnellsegment](assets/quick-segement.png)

## Segmentaufbau

Sie können auf den Segment Builder zugreifen, indem Sie auf das + -Symbol über der Segmentliste im Menü der linken Komponenten klicken oder aus dem Dropdown-Menü &quot;Komponenten&quot;auf Segment erstellen... klicken. Im Gegensatz zu den Schnellsegmenten stehen Ihnen hier alle Optionen zur Verfügung. Um mehrere Bedingungen hinzuzufügen, können Sie sequenzielle Segmente mit dem Operator &quot;then&quot;erstellen. Mit sequenziellen Segmenten können Sie auch &quot;logische Gruppe&quot;als Ebene (anstelle von Treffer, Besuch oder Besucher) verwenden. Mit Segment Builder können Sie den Segmenten auch eine Beschreibung hinzufügen. So können Sie Kontexte dazu hinzufügen, wer das Segment erstellt hat oder welche Datentypen für die Filterung erstellt wurden, oder sogar einfach &quot;Tags&quot;zum Segment hinzufügen, um Organisationszwecke zu erhalten, die beide im schnellen Segment-Builder nicht möglich sind.

Die Verwendung des Segmentaufbaus ist wichtig, wenn Ihr Segment mehr als 3 Bedingungen aufweisen soll, wenn Sie Container verwenden oder sequenzielle Segmente benötigen. Der vollständige Segment-Builder bietet viel mehr Optionen, um komplexere Segmente zu erstellen. Dies kann Ihnen helfen, verschiedene Kundentypen, Kategorien, Journey usw. aufzuschlüsseln. Nachdem diese Segmente erstellt und gespeichert wurden, werden sie zur Übergeordneten Segmentliste hinzugefügt, d. h. sie können getaggt, genehmigt, freigegeben, in mehreren Berichten verwendet und im Experience Cloud veröffentlicht werden. Durch die Veröffentlichung im Experience Cloud können Sie das Segment in anderen Adobe-Produkten verwenden, z. B. in Adobe Target für Personalisierungs-Targeting. Im Segment Builder erstellte Segmente können nicht im Bereich für schnelle Segmente bearbeitet werden. Sie müssen den Segment Builder öffnen, um Änderungen daran vorzunehmen. Glücklicherweise bietet die Vorschau rechts eine detailliertere Analyse des Traffics, den das Segment in den letzten 90 Tagen einbringen würde. Dies bedeutet, dass Sie einfacher sicherstellen können, dass das Segment das einbringt, was Sie möchten, bevor Sie speichern.

![Segmentaufbau](assets/segment-builder-quick.png)

## Nutzungsszenarios

In verschiedenen Branchen können Ihre Verwendungszwecke für das Erstellen benutzerdefinierter Segmente unterschiedlich sein. In der E-Commerce-Abteilung eines großen Einzelhändlers führen wir häufig Sondierungsanalysen durch, um festzustellen, welche Wege Kunden zum Kauf einschlagen. Wenn bei Aktionen wie dem Hinzufügen von Produkten zum Warenkorb oder dem Platzieren von Bestellungen Spitzen oder Rückgänge auftreten, kann die Verwendung der schnellen Segmente nützlich sein. Während einer Analyse kann ich schnell ein Segment für einen bestimmten Kundentyp oder für eine bestimmte Aktion/einen bestimmten Link erstellen, auf die/den sie klicken. Wenn ich den Segment Builder nicht öffnen und jedes Segment speichern muss, kann ich die Bedingungen schnell hinzufügen und sie dann genauso schnell entfernen. Dies spart viel Zeit, wenn Sie versuchen zu erklären, warum wir eine Änderung auf unserer Site sehen.

Alternativ dazu kann es manchmal vorkommen, dass der Segment Builder von mir besucht wurde. Nicht jeder Kunde ist derselbe, und oft möchten wir bestimmte Typen von Kunden betrachten, die durch von ihm durchgeführte Aktionen oder Pfade identifiziert werden. Mithilfe des Segment Builders können wir mehrere Bedingungen hinzufügen, um die verschiedenen Arten von Kunden zu identifizieren und die Segmente zu speichern, damit sie von mehreren Analysten freigegeben und verwendet werden können. Es ist wichtig, dass diese Segmenttypen in allen Berichten konsistent sind. Daher ist es besser, eine für alle geeigneten erstellte Version zu verwenden, als jede Person, die eine eigene Version erstellt, da die Ergebnisse unterschiedlich sein können.

Insgesamt sind sowohl die Schnellsegmente als auch der Segment Builder hervorragende Tools für Ihre Analyse. Sie haben jeweils ihre Ziele, Vorteile und Nachteile. Sehen Sie sich unsere nützlichen Tipps und Tricks-Tabellen unten an, um eine kurze Anleitung zu erhalten.

## Autor

Dieses Dokument wurde verfasst von:

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, Digital Analyst III bei Best Buy Canada

Adobe Analytics-Experte

## Download

[![Schnellsegmentdownload](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
