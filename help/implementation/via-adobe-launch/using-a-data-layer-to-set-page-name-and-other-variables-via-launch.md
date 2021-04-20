---
title: Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen in Adobe Analytics über den Start
description: Die Verwendung einer Datenschicht für Analytics und andere Experience Cloud-Lösungen wird als Best Practice betrachtet. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und sie in Launch verwenden, um Variablen in Adobe Analytics zu füllen.
feature: Launch Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: "Developer, Data Engineer"
level: Beginner
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 4%

---


# Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen über [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Die Verwendung einer Datenschicht für [!DNL Analytics] und andere Experience Cloud-Lösungen wird als Best Practice betrachtet. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und sie in [!DNL Experience Platform Launch] verwenden, um Variablen in Adobe Analytics zu füllen.

## Datenschichten {#data-layers}

Es empfiehlt sich, beim Arbeiten mit Daten auf Ihrer Site und mit Adobe Experience Cloud-Lösungen, insbesondere mit Adobe Analytics, eine Datenschicht zu verwenden. Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen. Die Datenschichten können von Verfolgungswerkzeugen (einschließlich Tag-Management-Systemen wie [!DNL Experience Platform Launch]) zum Ausfüllen von Berichten verwendet werden. Weitere Informationen zu Datenschichten finden Sie in der [Experience Cloud-Dokumentation](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) oder auf der [W3C-Site](https://www.w3.org/).

Weitere Informationen finden Sie im Blog [Datenschichten: Von Buzzword bis Best Practice,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), das Ihnen einige großartige Informationen über Datenschichten sowie einige Beispiele bietet.

## Datenschichten, [!DNL Experience Platform Launch] und Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Erstellen Sie einen Datenschichtstandard, der auf Ihrer Site verwendet werden soll und auf den [!DNL Experience Platform Launch] verweist.

   1. Legen Sie diese Datenschicht so hoch wie möglich im Kopf der Seite, bevor Sie [!DNL Experience Platform Launch] aufrufen, damit die Werte sofort von [!DNL Launch] und von Adoben-Lösungen, die hoch auf der Seite sein müssen, wie Adobe Target, verwendet werden können.

1. Füllen Sie die Daten in der Datenschicht.
1. Erstellen Sie in [!DNL Experience Platform Launch] &quot;[!UICONTROL Datenelemente]&quot;, die auf die Datenpunkte in der Datenschicht verweisen und die in [!DNL Experience Platform Launch] in [!UICONTROL Rules], [!UICONTROL Extensions] usw. verwendet werden können.
1. Verwenden Sie die [!UICONTROL Datenelemente] entweder in den globalen Variablen der [!DNL Analytics]-Erweiterung oder in einer Regel, indem Sie die Werte in [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] oder andere [!DNL Analytics]-Variablen zuweisen.
1. Trigger eines Beacons, das die Daten an [!DNL Analytics] sendet.

Das folgende Video führt Sie durch den Prozess.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
