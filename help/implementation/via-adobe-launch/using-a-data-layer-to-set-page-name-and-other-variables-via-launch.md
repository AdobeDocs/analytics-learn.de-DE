---
title: Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen in Adobe Analytics über den Start
description: Die Verwendung einer Datenschicht für Analytics und andere Experience Cloud-Lösungen wird als Best Practice betrachtet. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und sie in Launch verwenden, um Variablen in Adobe Analytics zu füllen.
feature: launch implementation
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
translation-type: tm+mt
source-git-commit: ee6c03cff5b051d9293d75965e9fd98f151d7fce
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 4%

---


# Verwenden einer Datenschicht zum Festlegen des Seitennamens und anderer Variablen über [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Die Verwendung einer Datenschicht für [!DNL Analytics] und andere Experience Cloud-Lösungen gilt als bewährtes Verfahren. In diesem Video erfahren Sie, wie Sie Ihre Werte aus der Datenschicht ziehen und sie zum Ausfüllen von Variablen in Adobe Analytics verwenden [!DNL Experience Platform Launch] können.

## Datenschichten {#data-layers}

Es empfiehlt sich, beim Arbeiten mit Daten auf Ihrer Site und mit Adobe Experience Cloud-Lösungen, insbesondere mit Adobe Analytics, eine Datenschicht zu verwenden. Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen. The data layers can be used by tracking tools (including tag management systems like [!DNL Experience Platform Launch]) to populate reports. Weitere Informationen zu Datenschichten finden Sie in der [Experience Cloud-Dokumentation](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) oder auf der [W3C-Site](https://www.w3.org/).

Siehe auch Blog- [Datenebenen: Von Buzzword bis Best Practice,](https://theblog.adobe.com/data-layers-buzzword-best-practice/)das Ihnen einige großartige Informationen über Datenschichten sowie einige Beispiele bietet.

## Datenschichten, [!DNL Experience Platform Launch]und Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Erstellen Sie einen Datenschichtstandard, der auf Ihrer Site verwendet werden soll und auf den Sie [!DNL Experience Platform Launch]verweisen können.

   1. Legen Sie diese Datenschicht so hoch wie möglich im Kopf der Seite, bevor Sie den Aufruf an [!DNL Experience Platform Launch]durchführen, damit die Werte sofort von [!DNL Launch]und von Adobe-Lösungen verwendet werden können, die hoch auf der Seite sein müssen, wie z. B. Adobe Target.

1. Füllen Sie die Daten in der Datenschicht.
1. Erstellen Sie in [!DNL Experience Platform Launch]diesem Fall &quot;[!UICONTROL Datenelemente]&quot;, die auf die Datenpunkte in der Datenschicht verweisen und die in allen [!DNL Experience Platform Launch] Regeln [!UICONTROL ,]Erweiterungen usw. verwendet werden können.
1. Verwenden Sie die [!UICONTROL Datenelemente] entweder in den globalen [!DNL Analytics] Erweiterungsvariablen oder in einer Regel und weisen Sie die Werte [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName]oder anderen [!DNL Analytics] Variablen zu.
1. Auslösen eines Beacons, in das die Daten gesendet werden [!DNL Analytics].

Das folgende Video führt Sie durch den Prozess.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
