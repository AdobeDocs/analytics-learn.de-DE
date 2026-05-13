---
title: Erstellen standardisierter Benennungskonventionen
description: Dabei gelten standardisierte Namenskonventionen owohl für den Variablennamen selbst, wenn er in der Admin-Benutzeroberfläche aktiviert ist, als auch für die Werte, die an die Dimension übergeben werden.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 0fe3b981-0d9b-4f12-a6ca-63a4140f4baf
TQID: https://experienceleague.adobe.com/nnAluH2AvqNbWEPk3lbthk-xDl-tnqyW8uHg4Beurq0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 78%

---

# Erstellen standardisierter Benennungskonventionen

**WAS:** Es gelten standardisierte Benennungskonventionen sowohl für den Variablennamen selbst, wenn er in der Admin-Benutzeroberfläche von Adobe Analytics (AA) aktiviert ist, als auch für die Werte, die an die Dimension übergeben werden. (d. h. Seitennamen wären „Seitenname (v1)“ als Variablenname, wobei die übergebenen Seitennamenwerte einheitlich sein und einer bestimmten Struktur/Hierarchie folgen sollten, etwa „Seitenname|Homepage“ oder „Seitenname|Suche|Suchergebnisse“).

**WARUM:** Namenskonventionen sind eine gute Möglichkeit, alles einheitlich zu halten und die Schnittstelle für Ihre Benutzer*innen leicht verständlich zu gestalten. Wenn Sie diese von Anfang an erstellen und in der Plattform und im Code durchsetzen, wird auch die Skalierung einfacher.

**WIE:** Die Schnittstelle und das Tagging-Dokument sollten sowohl für „Name“ als auch für „Beschreibung“ übereinstimmen. Dies erspart Ihren Benutzern das Aufrufen eines Excel-Dokuments und ermöglicht es ihnen, Ihre Daten direkt in der Schnittstelle zu verstehen. Aus Gründen der Konsistenz empfiehlt es sich außerdem, alles klein zu schreiben.

Es ist immer am besten, auch die Seitennamen (oder Bildschirmnamen für Apps) über die gesamte Plattform hinweg konsistent zu halten. Sie können beispielsweise `property:section:sub section:sub sub section:unique page name` in eine Variable/Dimension festlegen. Wenn alle diese Felder separate Felder in Ihrer Datenschicht sind, können Sie den Seitennamen sogar direkt in Ihrer JS-Datei bzw. in Launch erstellen. Die Festlegung aller Elemente in ihren eigenen Dimensionen kann Ihnen dabei helfen, bestimmte Eigenschaften oder Bereiche Ihrer Site/App einfacher aufzuschlüsseln und Traffic und Flüsse besser zu verstehen.

Alles, was es den Benutzer*innen erleichtert, die Daten zu finden und zu verstehen, einschließlich so einfacher Dinge wie Namenskonventionen, erhöht die Nutzung von Adobe Analytics und liefert bessere Einblicke für das Unternehmen.

## Autoren

An diesem Dokument haben mitgewirkt:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bei NortonLifeLock
Adobe Analytics-Experte

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant bei Adobe
