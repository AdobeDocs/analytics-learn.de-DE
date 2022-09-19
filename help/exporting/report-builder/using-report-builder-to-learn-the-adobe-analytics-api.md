---
title: Verwenden von Report Builder, um mehr über die Adobe Analytics-API zu erfahren
description: Wir alle kennen und lieben Report Builder. Was also, wenn ich Ihnen sage, dass Sie Ihre Kenntnisse rund um Report Builder nutzen können, um Ihre Adobe Analytics-Fähigkeiten noch weiter auszubauen? In diesem Video erfahren Sie, wie Sie Report Builder-Debugging-Anfragen ausführen und diese verwenden können, um zu lernen, wie Sie Ihre eigenen Analytics-API-Abfragen erstellen.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: User
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 100%

---

# Verwenden von [!UICONTROL Report Builder], um mehr über die Adobe Analytics-API zu erfahren {#using-report-builder-to-learn-the-adobe-analytics-api}

Wir alle kennen und lieben [!UICONTROL Report Builder]. Was also, wenn ich Ihnen sage, dass Sie Ihre Kenntnisse rund um [!UICONTROL Report Builder] nutzen können, um Ihre Adobe Analytics-Fähigkeiten noch weiter auszubauen? In diesem Video erfahren Sie, wie Sie [!UICONTROL Report Builder]-Debugging-Anfragen ausführen und diese verwenden können, um zu lernen, wie Sie Ihre eigenen [!DNL Analytics]-API-Abfragen erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**AKTUALISIERUNG**: Die Art und Weise, wie [!UICONTROL Report Builder] die Daten anfordert, wurde leicht aktualisiert. Sie können den in diesem Video gezeigten Ansatz weiterhin verwenden, aber die Informationen unterscheiden sich in einem Debugger geringfügig.

In einem Debugger:

1. Suchen Sie nach „api5.omniture.com“. Die Zahl variiert je nach Daten-Center zwischen 1 und 5.

2. Navigieren Sie zur Registerkarte [!UICONTROL Anfrage].

3. Suchen Sie in der Anfrage nach „[!DNL Report.Queue]“.

Es gibt auch eine alternative Methode zum Debugging von Anfragen wie dieser, die genauso gut funktioniert. Sie können die Protokollierung in [!UICONTROL Report Builder] über das Menü [!UICONTROL Optionen] einschalten. Auf diese Art werden dieselben Informationen erfasst wie bei einem Debugger. Protokolle finden Sie unter [!UICONTROL Dokumente] > [!UICONTROL ReportBuilderLogs]. Sie sind dort nach Tag organisiert. Sie können die Datei nach „Report.Queue“ durchsuchen, um jede Ihrer Anfragen zu finden. Protokolle helfen auch bei der Fehlerbehebung im Fall von Problemen.

Weitere Informationen zu dieser Funktion finden Sie in der [Dokumentation](https://www.adobe.io/).
