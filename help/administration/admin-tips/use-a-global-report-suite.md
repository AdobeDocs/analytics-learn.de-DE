---
title: Verwenden einer globalen Report Suite
description: Eine einzelne globale Report Suite kann auf vielerlei Weise helfen und Ihre Implementierung erheblich vereinfachen.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
exl-id: 490addfd-b810-4f15-b065-e0e58048c882
TQID: https://experienceleague.adobe.com/Gvyi3-9dJ3UXp3vaSIe0bhqswu2kSOW-EAorajxCq78
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 769
ht-degree: 98%

---

# Verwenden einer globalen Report Suite

**WAS:** Es ist verlockend, Report Suites für jede Ihrer Sites zu erstellen, aber dies kann schnell zu Ihrem schlimmsten Albtraum werden – sowohl in Bezug auf die Kompliziertheit Ihrer Berichterstattung als auch auf Ihre Implementierung. Eine einzelne globale Report Suite kann auf vielerlei Weise helfen und Ihre Implementierung erheblich vereinfachen.

**WARUM:** Das Erstellen einer globalen Report Suite ist die einzige Option, um eine einheitliche Ansicht Ihrer digitalen Eigenschaften und der Journey der Benutzer*innen für jede Eigenschaft zu erhalten. Wenn Sie über eine Mobile App und eine Website verfügen, sollten Sie die App-Daten und Webdaten immer in einer Report Suite kombinieren, um geräteübergreifende Journeys zu nutzen und diejenigen zu verfolgen, die beide Eigenschaften als Einzelbesucher*innen besuchen, im Vergleich zu separaten Report Suites, in denen Sie einen unzusammenhängenden Datensatz mit 2 Besucher*innen – 1 Besucher*in pro Eigenschaft – haben würden, ohne die Möglichkeit, die Überschneidung zu erkennen.

Im Folgenden finden Sie die Vor- und Nachteile einer einzelnen Report Suite, was Ihnen bei der Gewichtung Ihrer Optionen helfen kann:

* VORTEILE:
   * Ihre gesamte digitale Landschaft ist einfach zu verstehen. Wenn Sie die Dimension „Eigenschaften“ (eVar) implementiert haben und in anderen Tipps auf sie verwiesen wird, können Sie sehr einfach eine einzige Ansicht aller Ihrer Sites und Apps, Traffic und Konversionen erhalten. Dieser umfassende Überblick ist der Schlüssel zum Verständnis Ihres Geschäfts insgesamt.
   * Im selben Sinn können Sie nun sehen, wie Benutzer*innen sich durch all Ihre Eigenschaften bewegen, und ihre Journey in Ihrer digitalen Landschaft verstehen.
   * Einfachere Verwaltung. Bei der Verwendung mehrerer Report Suites müssen Sie die Benutzeroberfläche an mehreren Stellen pflegen sowie mehrere Tagging-Dokumente (oder ein komplizierteres) verwalten. Alles an einem Ort zu halten bedeutet, dass es nur einen Ort gibt, an dem Updates vorgenommen werden können. Außerdem wird die Zugangsgewährung viel einfacher.
   * Bessere Benutzerfreundlichkeit in der Benutzeroberfläche. Wenn Ihre Benutzer*innen nur einen Ort haben, müssen sie nicht darüber nachdenken, welche Report Suite sie auswählen sollen. Beachten Sie, dass Sie nicht mehrere Report Suites im selben Arbeitsbereich verwenden können. Wenn Sie mehrere davon haben, kann dies Ihre Benutzer*innen verwirren.
   * Weniger Server-Aufrufe = weniger Kosten. Wenn Sie mehrere Report Suites aufrufen, erhöhen sich Ihre Kosten. Wenn Sie Ihre Implementierung einfach halten, können Sie auch Ihre Kosten niedrig halten.
   * Sie können Virtual Report Suites (VRS) einfach nutzen, um Site-spezifische Daten innerhalb der globalen Report Suite auszuschlüsseln und Benutzerberechtigungen bei Bedarf auf der Grundlage einer VRS einzuschränken. Sobald Daten in einzelne Report Suites unterteilt sind, lassen sie sich nicht mehr aggregieren. Wenn sie jedoch bereits in einem Datensatz (globale RS) zusammengefasst sind, können sie einfach aufgeschlüsselt werden.
* NACHTEILE:
   * Wenn Sie über sehr stark getrennte Eigenschaften verfügen, bei denen Benutzer*innen nicht von einer zum anderen wechseln und dies nie erwartet wird, sollten Sie separate Report Suites beibehalten.
   * Wenn Ihre Eigenschaften sehr unterschiedliche Tagging- und Reporting-Anforderungen haben, kann es sinnvoll sein, im Interesse der Variableneffizienz separate Report Suites einzurichten. Separate Report Suites bieten Ihnen mehr Flexibilität bei der Verwendung benutzerdefinierter Variablen (mehr eVars).
   * Überschreiten individueller Werte: In der Adobe Analytics-Oberfläche können Sie für einen bestimmten Zeitraum innerhalb einer Dimension nur 500.000 individuelle Werte anzeigen. Sobald Sie diesen Wert überschreiten, werden die Werte in der Benutzeroberfläche mit dem Hinweis „Eindeutige Werte überschritten“ oder „geringer Traffic“ gruppiert. Diese Werte stehen Ihnen zwar weiterhin im Backend (d. h. Data Warehouse, Daten-Feeds) zur Verfügung, können jedoch nicht über die Benutzeroberfläche visualisiert werden. Wenn Sie sehr detaillierte Daten haben (z. B. Benutzer-ID, PSN usw.), kann diese Grenze leicht erreicht werden. Die Verwendung separater Report Suites kann bei diesem Problem hilfreich sein.

**WIE:** Mit einer neuen AA-Implementierung zu beginnen und eine globale Report Suite zu verwenden, ist einfach und unkompliziert. Sie müssen lediglich die globale Report Suite (eine für Entwicklung und eine für Produktion) in der Admin-Benutzeroberfläche von AA erstellen und dieselben Werte der Report Suite-ID (RSID) für alle Eigenschaften anwenden.

Die Migration von einer Multi-Tagging-Strategie mit einer eindeutigen Report Suite pro Eigenschaft erfordert mehr Strategie und Planung. Beachten Sie dabei die folgenden Aspekte:

* Ausrichten Ihrer Variablen (d. h. eVar1 auf Eigenschaft A muss denselben Datenpunkt erfassen wie eVar1 auf Eigenschaft B)
* Konsolidierung von Verarbeitungsregeln, Marketing-Kanalregeln, Klassifizierungen (SAINT und Rule Builder)
* Migration von Daten-Feeds und Datenquellen
* Auswahl eines Stichtags und Kommunikation dieses Datums mit allen Geschäftsbenutzer*innen

## Autoren

An diesem Dokument haben mitgewirkt:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bei NortonLifeLock
Adobe Analytics-Experte

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant bei Adobe
