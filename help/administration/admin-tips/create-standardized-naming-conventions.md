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
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 100%

---

# Erstellen standardisierter Benennungskonventionen

**WAS:** Es gelten standardisierte Benennungskonventionen sowohl für den Variablennamen selbst, wenn er in der Admin-Benutzeroberfläche von Adobe Analytics (AA) aktiviert ist, als auch für die Werte, die an die Dimension übergeben werden. (d. h. Seitennamen wären „Seitenname (v1)“ als Variablenname, wobei die übergebenen Seitennamenwerte einheitlich sein und einer bestimmten Struktur/Hierarchie folgen sollten, etwa „Seitenname|Homepage“ oder „Seitenname|Suche|Suchergebnisse“).

**WARUM:** Namenskonventionen sind eine gute Möglichkeit, alles einheitlich zu halten und die Schnittstelle für Ihre Benutzer*innen leicht verständlich zu gestalten. Wenn Sie diese von Anfang an erstellen und in der Plattform und im Code durchsetzen, wird auch die Skalierung einfacher.

**WIE:** Die Schnittstelle und das Tagging-Dokument sollten sowohl für „Name“ als auch für „Beschreibung“ übereinstimmen. Dies erspart Ihren Benutzer*innen das Aufrufen eines Excel-Dokuments und ermöglicht es ihnen, Ihre Daten direkt in der Schnittstelle zu verstehen. Aus Gründen der Konsistenz empfiehlt es sich außerdem, alles klein zu schreiben.

Es ist immer am besten, auch die Seitennamen (bzw. die Bildschirmnamen für Apps) über die gesamte Plattform hinweg konsistent zu halten. Sie können zum Beispiel „Eigenschaft:section:Unterabschnitt:Unterunterabschnitt:eindeutiger Seitenname“ in eine Variable/Dimension einfügen. Wenn alle diese Felder separate Felder in Ihrer Datenschicht sind, können Sie den Seitennamen sogar direkt in Ihrer JS-Datei bzw. in Launch erstellen. Die Festlegung aller Elemente in ihren eigenen Dimensionen kann Ihnen dabei helfen, bestimmte Eigenschaften oder Bereiche Ihrer Site/App einfacher aufzuschlüsseln und Traffic und Flüsse besser zu verstehen.

Alles, was es den Benutzer*innen erleichtert, die Daten zu finden und zu verstehen, einschließlich so einfacher Dinge wie Namenskonventionen, erhöht die Nutzung von Adobe Analytics und liefert bessere Einblicke für das Unternehmen.

## Autoren

An diesem Dokument haben mitgewirkt:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bei NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant bei Adobe
