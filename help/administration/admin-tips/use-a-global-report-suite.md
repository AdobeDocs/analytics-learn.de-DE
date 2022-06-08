---
title: Globale Report Suite verwenden
description: Eine einzelne globale Report Suite kann auf vielerlei Weise helfen und Ihre Implementierung wirklich vereinfachen.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---


# Globale Report Suite verwenden

**WAS:** Es ist verlockend, Report Suites für jede Ihrer Sites zu erstellen, aber dies kann schnell zu Ihrem schlimmsten Albtraum werden - sowohl was die Komplizierung Ihrer Berichterstellung als auch Ihre Implementierung betrifft. Eine einzelne globale Report Suite kann auf vielerlei Weise helfen und Ihre Implementierung wirklich vereinfachen.

**WARUM:** Das Erstellen einer globalen Report Suite ist die einzige Option, um eine einheitliche Ansicht Ihrer digitalen Eigenschaften und der Journey der Benutzer für jede Property zu erhalten. Wenn Sie über eine mobile App und eine Website verfügen, sollten Sie die App-Daten und Webdaten immer in einer Report Suite kombinieren, um geräteübergreifende Journey zu nutzen und diejenigen zu verfolgen, die beide Properties als Einzelbesucher besuchen, im Vergleich zu separaten Report Suites, in denen Sie einen unzusammenhängenden Datensatz mit 2 Besuchern - 1 Besuchern pro Property - ohne Kenntnis des Crossover haben würden.

Im Folgenden finden Sie die Vor- und Nachteile einer einzelnen Report Suite, die Ihnen bei der Gewichtung Ihrer Optionen hilft:

* PROS:
   * Ihre gesamte digitale Landschaft einfach zu verstehen. Wenn Sie die Dimension &quot;Eigenschaften&quot;(eVar) implementiert haben, auf die in anderen Tipps verwiesen wird, können Sie sehr einfach eine einzige Ansicht aller Ihrer Sites und Apps, Traffic und Konversionen erhalten. Dieser umfassende Überblick ist der Schlüssel zum Verständnis Ihres Unternehmens insgesamt.
   * Im selben Sinn können Sie nun sehen, wie Benutzer durch all Ihre Eigenschaften fließen, und ihre Journey in Ihrer digitalen Landschaft verstehen.
   * Einfachere Verwaltung. Bei der Verwendung mehrerer Report Suites müssen Sie die Benutzeroberfläche an mehreren Stellen sowie mehrere Tagging-Dokumente verwalten (oder eine kompliziertere). Alles an einem Ort zu halten bedeutet, dass es nur einen Ort gibt, an dem Updates vorgenommen werden können. Außerdem wird die Zugangsgewährung viel einfacher.
   * Bessere Benutzerfreundlichkeit in der Benutzeroberfläche. Wenn Ihre Benutzer nur einen Ort haben, müssen sie nicht darüber nachdenken, welche Report Suite ausgewählt werden soll. Beachten Sie, dass Sie nicht mehrere Report Suites im selben Arbeitsbereich verwenden können. Mehrere davon können Ihre Benutzer verwirren.
   * Weniger Server-Aufrufe = weniger Kosten. Wenn Sie mehrere Report Suites aufrufen, erhöhen Sie Ihre Kosten. Durch die einfache Implementierung werden auch Ihre Kosten niedrig gehalten.
   * Sie können Virtual Report Suites (VRS) einfach nutzen, um Site-spezifische Daten innerhalb der globalen Report Suite auszuschlüsseln und Benutzerberechtigungen bei Bedarf auf der Grundlage einer VRS einzuschränken. Sobald Daten in einzelne Report Suites unterteilt sind, können sie nicht mehr aggregiert werden. Wenn sie jedoch bereits in einem Datensatz (globale RS) zusammengefasst sind, können sie einfach aufgeschlüsselt werden.
* CONS:
   * Wenn Sie über sehr separate Eigenschaften verfügen, bei denen Benutzer nicht von einem zum anderen wechseln und dies nie erwartet wird, sollten Sie separate Report Suites beibehalten.
   * Wenn Ihre Eigenschaften sehr unterschiedliche Tagging- und Reporting-Anforderungen haben, kann es sinnvoll sein, separate Report Suites im Interesse der Variableneffizienz einzurichten. Separate Report Suites bieten Ihnen mehr Flexibilität bei der Verwendung benutzerdefinierter Variablen (mehr eVars).
   * Individuelle Werte überschritten: In der Adobe Analytics-Oberfläche können Sie für einen bestimmten Zeitraum nur 500.000 individuelle Werte innerhalb einer Dimension anzeigen. Sobald Sie diesen Wert überschreiten, werden die Werte in der Benutzeroberfläche als &quot;Individuelle Werte überschritten&quot;oder &quot;geringer Traffic&quot;gruppiert. Diese Werte stehen Ihnen zwar weiterhin im Backend zur Verfügung (d. h. Data Warehouse, Daten-Feeds), können jedoch nicht über die Benutzeroberfläche visualisiert werden. Wenn Sie sehr detaillierte Daten haben (z. B. Benutzer-ID, PSN usw.), ist es einfach, diese Ebene zu erreichen. Die Verwendung separater Report Suites kann bei diesem Problem hilfreich sein.

**WIE:** Die Verwendung einer einzigen globalen Report Suite ist einfach und unkompliziert. Sie müssen lediglich die globale Report Suite (eine für Entwicklung und eine für Produktion) in der Administrator-Benutzeroberfläche erstellen und dieselben Report Suite-ID (RSID)-Werte für alle Eigenschaften anwenden.

Die Migration von einer Multi-Tagging-Strategie mit einer eindeutigen Report Suite pro Eigenschaft erfordert mehr Strategie und Planung. Beachten Sie dabei einige Aspekte:

* Wenn Sie Ihre Variablen ausrichten (d. h. eVar 1 auf Property A), muss der gleiche Datenpunkt wie eVar 1 auf Property B erfasst werden.
* Konsolidierung von Verarbeitungsregeln, Marketing-Kanalregeln, Klassifizierungen (SAINT und Rule Builder)
* Migration von Daten-Feeds und Datenquellen
* Auswählen eines reduzierten Datums und Kommunikation mit allen Geschäftsbenutzern

## Autoren

Dieses Dokument wurde von folgenden Personen mitgeschrieben:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bei NortonLifeLock Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant bei Adobe
