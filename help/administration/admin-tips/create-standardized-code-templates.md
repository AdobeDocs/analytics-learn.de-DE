---
title: Erstellen standardisierter Code-Vorlagen
description: Für eine Basisimplementierung (d. h. für das, was Ihr Unternehmen als unerlässliche KPIs für alle Adobe Analytics-Sites betrachtet) sollte Ihre Organisation nach Möglichkeit eine einzige Implementierungsmethode verwenden.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: be00c8c0-a4bc-4380-98da-d1e2a3d31ec5
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 100%

---

# Erstellen standardisierter Code-Vorlagen

**WAS:** Für eine „Basisimplementierung“ (d. h. für das, was Ihr Unternehmen als unerlässliche KPIs für alle Adobe Analytics-Sites betrachtet) sollte Ihre Organisation nach Möglichkeit eine einzige Implementierungsmethode verwenden. Verwenden Sie beispielsweise die gleiche Site-übergreifende Datenschichtstruktur und nutzen Sie dieselbe Tag-Manager-Regel/denselben benutzerdefinierten Code, um Dinge wie interne Suchen oder Besucherprofilinformationen zu erfassen.

**WARUM:** Eine wiederholbare und skalierbare Basisimplementierung macht das Hinzufügen neuer Elemente oder neuer Websites/Programme zu einem rationellen, wenig aufwändigen Unterfangen und sorgt gleichzeitig für eine saubere Implementierung und einfache Fehlerbehebung. Die Verwendung einer einheitlichen Methode erleichtert es auch neuen Admins/Entwickler*innen, online zu gehen und zu verstehen, wormit sie arbeiten.

**WIE:** Verwenden Sie eine einzige Formatvorlage, die an Entwickler*innen übergeben werden kann, wenn eine neue Site- oder Tagging-Verbesserung online geht. Normalerweise funktioniert ein Word-Dokument gut, wenn Sie die folgenden Elemente umreißen können:

* Variablen, die implementiert werden, sowie deren Zweck und Zeitpunkt der Festlegung. Beispiel:

| AA-Variable | Beschreibung | Wann/wo sie festgelegt wird | Wie sie festgelegt wird |
|--- |--- |--- |--- |
| eVar8 | Interne Suchbegriffe | Auf der Landingpage der internen Suchergebnisse | Datenschicht |
| event8 | Anzahl der internen Suchen | Auf der Landingpage der internen Suchergebnisse | Startregel |

* Details zum Festlegen. Hier geben Sie die erforderlichen Datenschichtobjekte und deren Syntax sowie die zu konfigurierenden TMS-Regeln und die Details der Regeleinrichtung an.
* Testfälle, um sicherzustellen, dass sie in der Qualitätssicherung behandelt werden, sowie alle Variablen, die Sie in einem erfolgreichen Testfall erwarten. Erläutern Sie, was eine erfolgreiche Implementierung enthalten sollte, wenn die Entwickler*innen diese Verbesserung testen.

Idealerweise muss dieses Dokument dann nur für die nächste Site optimiert werden, auf der Sie die Grundlagen wie Eigenschaftsname, Seitenbenennungskonvention usw. aktualisieren. Es ist nicht erforderlich, das Rad jedes Mal neu zu erfinden, und Sie können mehr Zeit sparen.

## Autoren

An diesem Dokument haben mitgewirkt:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bei NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant bei Adobe
