---
title: Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen in Adobe Analytics via Launch
description: Die Verwendung einer Datenschicht für Analytics und andere Experience Cloud-Lösungen gilt als Best Practice. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und in Launch verwenden, um Variablen in Adobe Analytics damit zu befüllen.
feature: Launch Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: ht
source-wordcount: '365'
ht-degree: 100%

---

# Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Verwenden einer Datenschicht für [!DNL Analytics] und andere Experience Cloud-Lösungen gilt als Best Practice. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und in [!DNL Experience Platform Launch] verwenden, um Variablen in Adobe Analytics damit zu befüllen.

## Datenschichten {#data-layers}

Es gilt als Best Practice, beim Arbeiten mit Daten auf Ihrer Site und in Adobe Experience Cloud-Lösungen, insbesondere mit Adobe Analytics, eine Datenschicht zu verwenden. Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen. Datenschichten können von Tracking-Tools (einschließlich Tag-Management-Systemen wie [!DNL Experience Platform Launch]) verwendet werden, um Berichte auszufüllen. Weitere Informationen zu Datenschichten finden Sie in der [Dokumentation zu Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=de) oder auf der [W3C-Site](https://www.w3.org/).

Weitere Informationen finden Sie im Blog-Artikel [Datenschichten: Vom Schlagwort zur Best Practice](https://theblog.adobe.com/data-layers-buzzword-best-practice/), der Ihnen einige gute Informationen zu Datenschichten und auch einige Beispiele liefert.

## Datenschichten, [!DNL Experience Platform Launch], und Adobe Analytics (oje?) {#data-layers-launch-and-adobe-analytics-oh-my}

1. Erstellen Sie einen Datenschichtenstandard zur Verwendung auf Ihrer Site, der durch [!DNL Experience Platform Launch] referenziert werden kann.

   1. Platzieren Sie diese Datenschicht so weit oben wie möglich im Kopf der Seite, bevor der Aufruf an [!DNL Experience Platform Launch] erfolgt, sodass die Werte sofort von [!DNL Launch] und von Adobe-Lösungen wie Adobe Target, die weit oben auf der Seite weit oben sein müssen, verwendet werden können.

1. Füllen Sie die Daten in der Datenschicht.
1. Erstellen Sie in [!DNL Experience Platform Launch] [!UICONTROL Datenelemente], die auf die Datenpunkte in der Datenschicht verweisen und die überall in [!DNL Experience Platform Launch] in [!UICONTROL Regeln], [!UICONTROL Erweiterungen] usw. verwendet werden können.
1. Verwenden Sie die [!UICONTROL Datenelemente] entweder in globalen Variablen von [!DNL Analytics] oder in einer Regel und sorgen Sie so dafür, dass die Werte [!UICONTROL Props], [!UICONTROL eVars], [!UICONTROL pageName] oder anderen [!DNL Analytics]-Variablen zugewiesen werden.
1. Lösen Sie ein Beacon aus, das die Daten an [!DNL Analytics] sendet.

Das folgende Video führt Sie durch den Prozess.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
