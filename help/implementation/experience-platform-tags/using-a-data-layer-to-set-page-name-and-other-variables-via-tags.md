---
title: Verwenden einer Datenschicht zum Festlegen von Analytics-Variablen in Experience Platform [!DNL tags]
description: Erfahren Sie, wie Sie eine Datenschicht zum Sourcing von Analytics-Daten und anderen Experience Cloud-Lösungen verwenden.
feature: Tags
topics: Development
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: a45667a8d7ccb46b9e33bd11a78fac9714a61df5
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 50%

---

# Verwenden einer Datenschicht zum Festlegen von Analytics-Variablen in Experience Platform [!DNL tags]

Verwenden einer Datenschicht für [!DNL Analytics] und andere Experience Cloud-Lösungen gilt als Best Practice. In diesem Video erfahren Sie, wie Sie Werte aus der Datenschicht abrufen und in Experience Platform verwenden können. [!DNL tags] , um Variablen in Adobe Analytics zu füllen.

## Datenschichten

Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler zu digitalen Webseiten hinzufügen. Analytics-Lösungen verwenden die Datenschicht letztendlich, um Werte in Berichte einzufügen. Tag-Management-Systeme, einschließlich Experience Platform [!DNL tags]) sind die Vermittler, die die Datenschicht lesen, die Werte Variablen zuordnen und diese Daten an digitale Erlebnislösungen senden.

Zusätzliche Informationen zu Datenschichten in der [Experience Cloud-Dokumentation](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=de).

## Datenschichten, Experience Platform [!DNL tags]und Adobe Analytics

1. Bestimmen oder identifizieren Sie einen Datenschicht-Standard, der auf Ihrer Site verwendet werden soll.

   1. Positionieren Sie die Datenschicht so weit wie möglich im Kopfabschnitt der Seite und vor dem Aufruf von Experience Platform. [!DNL tags]. Dadurch wird sichergestellt, dass der Zugriff auf die Werte sofort über [!DNL tags] und Adobe-Lösungen erfolgt, die sich hoch oben auf der Seite befinden, wie etwa Adobe Target.

1. Füllen Sie die Daten in der Datenschicht.
1. In Experience Platform [!DNL tags], erstellen Sie &quot;[!UICONTROL Datenelemente]&quot;, das die Datenpunkte in der Datenschicht zuordnet. Diese Datenelemente werden während des gesamten Experience Platform verwendet [!DNL tags] in [!UICONTROL Regeln] und [!UICONTROL Erweiterungen].
1. Weisen Sie die Werte in [!UICONTROL Datenelementen] entweder in der [!DNL Analytics]-Erweiterung im Bereich für globale Variablen oder in einer [!DNL Tags rule] [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] und anderen [!DNL Analytics]-Variablen zu.
1. Lösen Sie ein Beacon aus, das die Daten an [!DNL Analytics] sendet.

Das folgende Video führt Sie durch den Prozess.

>[!NOTE]
>
> Launch ist jetzt **[!DNL tags]**

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>Die in diesem Video verwendete Datenschicht mag zwar für Ihr Unternehmen nicht ideal sein. Aber das Konzept der Verwendung einer Datenschicht für das Übertragen wichtiger Daten in Ihre digitalen Marketing-Lösungen ist Best Practice.
