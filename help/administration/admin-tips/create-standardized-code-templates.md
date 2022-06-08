---
title: Erstellen standardisierter Codevorlagen
description: 'Für eine Basisimplementierung (d. h. was Ihr Unternehmen als die Muss-aufweist KPIs für alle Adobe Analytics-Sites betrachtet) sollte Ihre Organisation nach Möglichkeit über eine einzige Implementierungsmethode verfügen. '
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 2%

---


# Erstellen standardisierter Codevorlagen

**WAS:** Bei einer &quot;Grundlinien&quot;-Implementierung (d. h. was Ihr Unternehmen als die erforderlichen KPIs für alle Adobe Analytics-Sites betrachtet) sollte Ihre Organisation nach Möglichkeit über eine einzige Implementierungsmethode verfügen. Verwenden Sie beispielsweise die gleiche Site-übergreifende Datenschichtstruktur und nutzen Sie dieselbe Tag-Manager-Regel/denselben benutzerdefinierten Code, um Dinge wie interne Suchen oder Besucherprofilinformationen zu erfassen.

**WARUM:** Durch eine wiederholbare und skalierbare Basisimplementierung wird das Hinzufügen neuer Elemente oder neuer Sites/Apps zu einem optimierten, minimalen Aufwand, während Sie Ihre Implementierung sauber und einfach zu beheben halten. Die Verwendung einer einheitlichen Methode erleichtert es auch neuen Administratoren/Entwicklern, online zu gehen und zu verstehen, wormit sie arbeiten.

**WIE:** Nehmen Sie eine Vorlage für ein einzelnes Format an, die an Entwickler übergeben wird, wenn eine neue Site- oder Tagging-Verbesserung online geht. Normalerweise funktioniert ein Word-Dokument gut, wenn Sie die folgenden Elemente umreißen können:

* Variablen, die implementiert werden, deren Zweck und Zeitpunkt der Festlegung. Beispiel:

| AA-Variable | Beschreibung | Wann/Wo wird festgelegt? | Festlegen |
|--- |--- |--- |--- |
| eVar8 | Interne Suchbegriffe | Auf der Landingpage der internen Suchergebnisse | Datenschicht |
| event8 | Anzahl der internen Suchen | Auf der Landingpage der internen Suchergebnisse | Launch-Regel |

* Details zum Festlegen. Hier geben Sie die erforderlichen Datenschichtobjekte und deren Syntax sowie die zu konfigurierenden TMS-Regeln und die Details der Regeleinrichtung an.
* Testfälle, um sicherzustellen, dass sie in der Qualitätssicherung behandelt werden, sowie alle Variablen, die Sie in einem erfolgreichen Testfall erwarten. Erläutern Sie, was eine erfolgreiche Implementierung enthalten sollte, wenn der Entwickler diese Verbesserung testet.

Idealerweise muss dieses Dokument nur für die nächste Site optimiert werden, auf der Sie die Grundlagen wie Eigenschaftsname, Seitenbenennungskonvention usw. aktualisieren. Es ist nicht erforderlich, das Rad jedes Mal neu zu erfinden, und Sie können mehr Zeit sparen.

## Autoren

Dieses Dokument wurde von folgenden Personen mitgeschrieben:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bei NortonLifeLock Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant bei Adobe
