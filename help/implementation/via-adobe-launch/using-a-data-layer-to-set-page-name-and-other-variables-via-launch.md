---
title: Verwenden einer Datenschicht zum Festlegen von Analytics-Variablen über Tags
description: Erfahren Sie mehr über die Verwendung einer Datenschicht für die Beschaffung von Analytics-Daten und anderen Experience Cloud-Lösungen.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 9%

---

# Verwenden Sie eine Datenschicht, um Analytics-Variablen über festzulegen. [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Verwenden einer Datenschicht für [!DNL Analytics] und anderen Experience Cloud-Lösungen eine Best Practice. In diesem Video erfahren Sie, wie Sie Werte aus der Datenschicht ziehen und in [!DNL Experience Platform Tags] , um Variablen in Adobe Analytics zu füllen.

## Datenschichten {#data-layers}

A _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler digitalen Webseiten hinzufügen. Analytics-Lösungen verwenden letztendlich die Datenschicht, um Berichte zu füllen. Tag-Management-Systeme, einschließlich [!DNL Experience Platform Tags]) sind die Vermittler, die die Datenschicht lesen, die Werte Variablen zuordnen und diese Daten an digitale Erlebnislösungen senden.

Zusätzliche Informationen zu Datenschichten in der [Dokumentation zu Experience Clouden](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=de) und der Blog [Datenschichten: Von Buzzword zu Best Practice](https://blog.adobe.com/en/2014/03/13/data-layers-buzzword-best-practice).

## Datenschichten, [!DNL Experience Platform Tags]und Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Definieren oder identifizieren Sie einen Datenschichtstandard, der auf Ihrer Site verwendet werden soll.

   1. Positionieren Sie die Datenschicht so weit wie möglich im Kopfabschnitt der Seite und vor dem Aufruf von [!DNL Experience Platform Tags]. Dadurch wird sichergestellt, dass der Zugriff auf die Werte sofort über [!DNL Tags] und durch Adobe-Lösungen, die auf der Seite besonders wichtig sein müssen, wie Adobe Target.

1. Füllen Sie die Daten in der Datenschicht.
1. In [!DNL Experience Platform Tags], erstellen Sie &quot;[!UICONTROL Datenelemente]&quot;, das die Datenpunkte in der Datenschicht zuordnet. Diese Datenelemente werden überall verwendet [!DNL Experience Platform Tags] in [!UICONTROL Regeln] und [!UICONTROL Erweiterungen].
1. In der [!DNL Analytics] Abschnitt mit den globalen Variablen der Erweiterung oder in einer [!DNL Tags rule], weisen Sie die Werte in [!UICONTROL Datenelemente] nach [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName], und anderen [!DNL Analytics] Variablen.
1. Lösen Sie ein Beacon aus, das die Daten an [!DNL Analytics] sendet.

Das folgende Video führt Sie durch den Prozess.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)

>[!NOTE]
>
>Die in diesem Video verwendete spezifische Datenschicht wird für Ihr Unternehmen möglicherweise nicht als &quot;Best Practice&quot;betrachtet. Das Konzept der Verwendung einer Datenschicht für das Aufdecken wichtiger Daten in Ihren digitalen Marketinglösungen ist Best Practice.