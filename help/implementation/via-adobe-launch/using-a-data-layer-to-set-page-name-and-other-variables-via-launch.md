---
title: Verwenden einer Datenschicht zum Festlegen von Analytics-Variablen mithilfe von Tags
description: Erfahren Sie mehr über die Verwendung einer Datenschicht zur Nutzung von Analytics-Daten und anderen Experience Cloud-Lösungen.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 100%

---

# Verwenden einer Datenschicht zum Festlegen von Analytics-Variablen mithilfe von [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Verwenden einer Datenschicht für [!DNL Analytics] und andere Experience Cloud-Lösungen gilt als Best Practice. In diesem Video erfahren Sie, wie Sie Werte aus der Datenschicht abrufen und in [!DNL Experience Platform Tags] verwenden können, um damit Variablen in Adobe Analytics zu befüllen.

## Datenschichten {#data-layers}

Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler zu digitalen Webseiten hinzufügen. Analytics-Lösungen verwenden die Datenschicht letztendlich, um Werte in Berichte einzufügen. Tag-Management-Systeme, einschließlich [!DNL Experience Platform Tags], dienen zur Vermittlung. Sie lesen die Datenschicht, ordnen die Werte Variablen zu und senden diese Daten an digitale Experience-Lösungen.

Weitere Informationen zu Datenschichten finden Sie in der [Dokumentation zu Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=de) und im Blog [Data Layers: From Buzzword to Best Practice](https://blog.adobe.com/en/2014/03/13/data-layers-buzzword-best-practice).

## Datenschichten, [!DNL Experience Platform Tags] und Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Bestimmen oder identifizieren Sie einen Datenschicht-Standard, der auf Ihrer Site verwendet werden soll.

   1. Positionieren Sie die Datenschicht möglichst hoch im Kopfabschnitt der Seite und vor dem Aufruf von [!DNL Experience Platform Tags]. Dadurch wird sichergestellt, dass der Zugriff auf die Werte sofort über [!DNL Tags] und Adobe-Lösungen erfolgt, die sich hoch oben auf der Seite befinden, wie etwa Adobe Target.

1. Füllen Sie die Daten in der Datenschicht.
1. Erstellen Sie in [!DNL Experience Platform Tags] „[!UICONTROL Datenelemente]“, mit denen die Datenpunkte in der Datenschicht zugeordnet werden. Diese Datenelemente werden überall in [!DNL Experience Platform Tags] in [!UICONTROL Regeln] und [!UICONTROL Erweiterungen] verwendet.
1. Weisen Sie die Werte in [!UICONTROL Datenelementen] entweder in der [!DNL Analytics]-Erweiterung im Bereich für globale Variablen oder in einer [!DNL Tags rule] [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] und anderen [!DNL Analytics]-Variablen zu.
1. Lösen Sie ein Beacon aus, das die Daten an [!DNL Analytics] sendet.

Das folgende Video führt Sie durch den Prozess.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>Die in diesem Video verwendete Datenschicht mag zwar für Ihr Unternehmen nicht ideal sein. Aber das Konzept der Verwendung einer Datenschicht für das Übertragen wichtiger Daten in Ihre digitalen Marketing-Lösungen ist Best Practice.