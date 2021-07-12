---
title: Verwenden einer Datenschicht zum Festlegen des Seitennamen und anderer Variablen in Adobe Analytics über Launch
description: Die Verwendung einer Datenschicht für Analytics und andere Experience Cloud-Lösungen gilt als Best Practice. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und in Launch verwenden, um Variablen in Adobe Analytics zu füllen.
feature: Implementierung starten
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 7%

---

# Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Die Verwendung einer Datenschicht für [!DNL Analytics] und andere Experience Cloud-Lösungen gilt als Best Practice. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und in [!DNL Experience Platform Launch] verwenden, um Variablen in Adobe Analytics zu füllen.

## Datenschichten {#data-layers}

Es empfiehlt sich, beim Arbeiten mit Daten auf Ihrer Site und Adobe Experience Cloud-Lösungen, insbesondere mit Adobe Analytics, eine Datenschicht zu verwenden. Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen. Die Datenschichten können von Tracking-Tools (einschließlich Tag-Management-Systemen wie [!DNL Experience Platform Launch]) verwendet werden, um Berichte zu füllen. Weitere Informationen zu Datenschichten finden Sie in der [Experience Cloud-Dokumentation](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) oder auf der [W3C-Site](https://www.w3.org/).

Weitere Informationen finden Sie im Blog [Datenschichten: Von Buzzword zu Best Practice,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), das Ihnen einige großartige Informationen über Datenschichten sowie einige Beispiele bietet.

## Datenschichten, [!DNL Experience Platform Launch] und Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Erstellen Sie einen Datenschichtstandard zur Verwendung auf Ihrer Site, der von [!DNL Experience Platform Launch] referenziert werden kann.

   1. Platzieren Sie diese Datenschicht so weit wie möglich im Seitenkopf vor dem Aufruf von [!DNL Experience Platform Launch], damit die Werte sofort von [!DNL Launch] und von Adobe-Lösungen, die auf der  stehen müssen, wie Adobe Target, verwendet werden können.

1. Füllen Sie die Daten in der Datenschicht.
1. Erstellen Sie in [!DNL Experience Platform Launch] &quot;[!UICONTROL Datenelemente]&quot;, die auf die Datenpunkte in der Datenschicht verweisen und die in [!DNL Experience Platform Launch] in [!UICONTROL Regeln], [!UICONTROL Erweiterungen] usw. verwendet werden können.
1. Verwenden Sie die [!UICONTROL Datenelemente] in den globalen Variablen der [!DNL Analytics]-Erweiterung oder in einer Regel, indem Sie die Werte [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] oder anderen [!DNL Analytics]-Variablen zuweisen.
1. Trigger eines Beacons, das die Daten an [!DNL Analytics] sendet.

Das folgende Video führt Sie durch den Prozess.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
