---
title: 'Verwenden von Best Practices bei der Verfolgung von Einzelseitenanwendungen (SPA) in Adobe Analytics '
description: In diesem Dokument beschreiben wir einige Best Practices, die Sie befolgen sollten und die Sie kennen sollten, wenn Sie Adobe Analytics zur Verfolgung von Einzelseitenanwendungen (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung von Experience Platform Launch, der empfohlenen Implementierungsmethode.
feature: implementation basics
topics: spa
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
translation-type: tm+mt
source-git-commit: 548ac75589383dfd4da4ae02412de91a0a3b28d6
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 0%

---


# Verwenden von Best Practices bei der Verfolgung von Einzelseitenanwendungen (SPA) in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In diesem Dokument beschreiben wir einige Best Practices, die Sie befolgen sollten und die Sie kennen sollten, wenn Sie Adobe Analytics zur Verfolgung von Einzelseitenanwendungen (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung von Adobe [!DNL Experience Platform Launch], der empfohlenen Implementierungsmethode.

ERSTE HINWEISE:

* Die folgenden Elemente gehen davon aus, dass Sie [!DNL Experience Platform Launch] zur Implementierung auf Ihrer Site verwenden. Die Überlegungen bestehen weiterhin, wenn Sie nicht verwenden [!DNL Experience Platform Launch], müssen sie jedoch an Ihre Implementierungsmethode anpassen.
* Da alle SPA unterschiedlich sind, müssen Sie möglicherweise einige der folgenden Punkte anpassen, um Ihren Anforderungen am besten zu entsprechen. Wir wollten jedoch einige Best Practices mit Ihnen austauschen. Dinge, über die Sie bei der Implementierung von Adobe Analytics auf SPA-Seiten nachdenken müssen.

## Einfache Darstellung der Arbeit mit SPAs in [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![SPA für Analysen beim Start](assets/spa_for_analyticsinlaunch.png)

**HINWEIS:** Wie angegeben, wird hier ein vereinfachtes Diagramm zur Handhabung von SPA-Seiten in einer Adobe Analytics-Implementierung mit [!DNL Experience Platform Launch]verwendet. In den folgenden Abschnitten dieser Seite besprechen wir die Schritte und alle Fragen, die Sie sorgfältig prüfen oder bearbeiten sollten.

## Festlegen der Datenschicht {#setting-the-data-layer}

Wenn neue Inhalte auf eine SPA-Seite geladen werden oder wenn eine Aktion auf einer SPA-Seite stattfindet, sollten Sie als Erstes die Datenschicht aktualisieren. Dies muss geschehen, BEVOR das benutzerdefinierte Ereignis Regeln auslöst [!DNL Experience Platform Launch], damit die neuen Werte aus der Datenschicht abgerufen und in Adobe Analytics gepusst werden [!DNL Experience Platform Launch] können.

Im Folgenden finden Sie eine Beispieldatenschicht, deren Elemente bei Änderung der Ansicht oder Aktion in Ihrer SPA geändert werden können. Bei einer Änderung im Vollbildmodus/Mehrheitsbildschirm wäre es üblich, ein &quot;[!DNL pageName]&quot;-Element zu ändern, sodass das neue Element in Adobe Analytics erfasst [!DNL Experience Platform Launch] und gesendet werden kann.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Experience Platform Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>
```

## Festlegen benutzerdefinierter Ereignis und Zuhören in [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Wenn neue Inhalte auf der Seite geladen werden oder wenn eine Aktion auf der Site stattfindet, sollten Sie informiert werden, [!DNL Experience Platform Launch] damit eine Regel ausgeführt und Daten an [!DNL Analytics]gesendet werden können. Es gibt verschiedene Möglichkeiten, dies zu tun: [!UICONTROL Direktaufrufregeln] oder [!UICONTROL benutzerspezifische Ereignis] .

* [!UICONTROL Direktaufruf] - [!UICONTROL Regeln]: in [!DNL Experience Platform Launch]können Sie eine [!UICONTROL Direktaufruf] - [!UICONTROL Regel] einrichten, die ausgeführt wird, wenn sie direkt von der Seite aufgerufen wird. Wenn das Laden Ihrer Seite oder Ihre Aktion auf Ihrer Site sehr einfach ist oder sie eindeutig ist und Sie jedes Mal einen bestimmten Satz von Anweisungen ausführen können ( [!DNL eVar4] auf X eingestellt und [!DNL event2] jedes Mal ausgelöst), können Sie eine [!UICONTROL Direktaufrufregel] - [!UICONTROL Regel]verwenden. Siehe [!DNL Experience Platform Launch] Dokumentation zum Erstellen von [!UICONTROL Direktaufrufregeln] - [!UICONTROL Regeln].
* Benutzerspezifische Ereignis: Für mehr Funktionalität und für die dynamische Zuweisung einer Nutzlast mit verschiedenen Werten sollten Sie benutzerdefinierte JavaScript-Ereignis einrichten und auf diese abhören, [!DNL Experience Platform Launch]in denen Sie die Nutzlast verwenden können, um Variablen festzulegen und die Daten an Adobe Analytics zu senden. Es ist wahrscheinlicher, dass Sie diese Funktion benötigen, und daher gilt diese Option als Best Practice. Jede Funktion auf Ihrer Site kann jedoch bestimmen, welche Methode am besten geeignet ist. Wir werden in diesem Dokument vorankommen, vorausgesetzt, Sie müssen diese Methode für benutzerspezifische Ereignis verwenden.

**Beispiele:** In [DIESEM](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) Hilfe-Dokument finden Sie Links zu Beispielsites für SPA, die implementiert wurden [!DNL Analytics] (und anderen Experience Cloud-Lösungen), sowie Dokumente, die beschreiben, was implementiert wurde. In diesen SPA-Beispielen wurden die folgenden benutzerspezifischen Ereignis verwendet:

* [!DNL event-view-start]: Dieses Ereignis sollte auf dem Beginn der Ansicht der Ansicht/des Status, die geladen wird, ausgelöst werden.
* [!DNL event-view-end]: Dieses Ereignis sollte auch dann ausgelöst werden, wenn eine Ansicht-/Statusänderung stattgefunden hat und alle SPA-Komponenten auf der Seite vollständig geladen wurden. Dies ist das Ereignis, das normalerweise einen Aufruf an Adobe Analytics auslöst.
* [!DNL event-action-trigger]: Dieses Ereignis sollte ausgelöst werden, wenn ein Ereignis auf der Seite auftritt, mit Ausnahme der Ansicht-/Statusladung. Dies kann ein Klick-Ereignis oder eine kleinere Inhaltsänderung ohne Änderung der Ansicht sein.

Weitere Informationen dazu, wie und wann diese ausgelöst werden, finden Sie auf den oben genannten Seiten/Dokumenten. Sie müssen nicht dieselben Ereignis verwenden, aber die hier aufgelisteten Funktionen sind empfohlene Best Practices. Das folgende Video zeigt eine Beispielsite und wo Sie nach benutzerdefinierten Ereignissen suchen [!DNL Experience Platform Launch] können.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ausführen von s.t() oder s.tl() in der [!DNL Experience Platform Launch] [!UICONTROL Regel] {#running-s-t-or-s-tl-in-the-launch-rule}

Eines der wichtigsten Dinge, die [!DNL Analytics] bei der Arbeit mit einem SPA zu verstehen sind, ist der Unterschied zwischen `s.t()` und `s.tl()`. Sie werden eine dieser Methoden auslösen, um Daten [!DNL Experience Platform Launch] [!DNL Analytics]an zu senden, aber Sie müssen wissen, wann jede gesendet werden soll.

* **s.t()** - &quot;t&quot;steht für &quot;track&quot;und ist eine normale Ansicht. Ändert sich die Ansicht, auch wenn sich die URL möglicherweise nicht ändert, so sehr, dass Sie sie als neue &quot;Seite&quot; *betrachten* würden? Ist dies der Fall, legen Sie &quot;s&quot;fest.[!DNL pageName] und verwenden, `s.t()` um den Aufruf an [!DNL Analytics]

* **s.tl()** - &quot;tl&quot;steht für &quot;track link&quot;und wird normalerweise zur Verfolgung von Klicks oder kleinen Inhaltsänderungen auf der Seite verwendet, im Gegensatz zu einer Vollbildänderung. Wenn die Änderung auf Ihrer Seite klein ist, damit Sie sie nicht als vollständige neue &quot;Seite&quot;betrachten, verwenden Sie die Variable s.pageName `s.tl()` und machen Sie sich keine Gedanken darüber, wie Sie sie ignorieren [!DNL Analytics] können.

**TIPP:** Manche Leute verwenden eine allgemeine Richtlinie, dass der Bildschirm, wenn er sich um mehr als 50 % ändert, als Ansicht und Verwendung von Seiten betrachtet werden sollte `s.t()`. Wenn die Änderung am Bildschirm weniger als 50 % beträgt, verwenden Sie `s.tl()`. Es liegt jedoch ganz bei Ihnen und was Sie als neue &quot;Seite&quot;betrachten und wie Sie Ihre Site in Adobe Analytics verfolgen möchten.

Im folgenden Video wird gezeigt, wo und wie das Launch by Adobe ausgelöst wird `s.t()` oder `s.tl()` .

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Variablen löschen {#clearing-variables}

Bei der Verfolgung Ihrer Site mit Adobe Analytics möchten Sie natürlich nur die richtigen Daten zum richtigen Zeitpunkt senden [!DNL Analytics] . In einer SPA-Umgebung kann ein Wert, der in einer [!DNL Analytics] Variablen verfolgt wird, bestehen bleiben und erneut gesendet werden, [!DNL Analytics]möglicherweise, wenn wir nicht mehr möchten, dass er gesendet wird. Aus diesem Grund gibt es in der [!DNL Analytics] Erweiterung eine Funktion zum Löschen der Variablen, sodass Sie eine neue Tonspur haben, wenn Sie die nächste Bildanforderung ausführen und Daten senden [!DNL Launch] [!DNL Analytics].

Im obigen Diagramm haben wir es am Ende des Prozesses aufgelistet, wobei die Variablen gelöscht werden, *nachdem* Sie den Treffer gesendet haben. In Wirklichkeit kann dies entweder vor ODER nach dem Senden des Treffers erfolgen, sollte jedoch in Ihren [!DNL Experience Platform Launch] Regeln konsistent sein, sodass Sie immer vor oder nach dem Festlegen von Variablen löschen und sie senden. Denken Sie daran, wenn Sie die Variablen *vor* der Ausführung löschen `s.t()`möchten, stellen Sie sicher, dass Sie zuerst die Variablen löschen, dann die neuen Variablen einstellen und schließlich die neuen Daten senden [!DNL Analytics].

**HINWEIS:** Das Löschen von Variablen ist bei der Ausführung nicht immer erforderlich, `s.tl()`da `s.tl()` die Variable jedes Mal neben der Variablen verwendet werden muss, um festzustellen, [!DNL linkTrackVars] welche Variablen festgelegt werden (automatisch hinter den Kulissen hinzugefügt [!DNL Analytics] [!DNL Experience Platform Launch]). Dies bedeutet, dass fehlerhafte Variablen normalerweise nicht bei der Verwendung eingehen, `s.tl()`aber bei der Verwendung `s.t()` in einer SPA-Umgebung wird dies sehr empfohlen. Trotzdem möchte ich empfehlen, die Funktion &quot;Clear Variables&quot;sowohl für eine SPA-Umgebung als auch für eine solche zu verwenden, um eine qualitativ hochwertige Datenerfassung sicherzustellen. Dies ist eine bewährte Methode, die die Verwendung der Funktion Clear Variables vorsieht `s.t()` und auch `s.tl()` in einer SPA- ermöglicht.

Das folgende Video zeigt, wo/wie die Variablen gelöscht werden [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Weitere zu berücksichtigende Aspekte {#additional-considerations}

### Fenster &quot;Benutzerdefinierter Code&quot;in [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

In der [!DNL Launch] [!DNL Analytics] Erweiterung können Sie an zwei Stellen benutzerdefinierten Code einfügen: Der Abschnitt [!UICONTROL Bibliotheksverwaltung] und der zusätzliche Abschnitt &quot;Tracker mit benutzerdefiniertem Code[!UICONTROL konfigurieren&quot;].

![Benutzerdefinierte Codefenster von Analytics starten](assets/launch_analyticscustomcodewindows.png)

Es ist wichtig zu wissen, dass einer dieser Orte den Code in ihnen nur einmal ausführen wird, wenn das Laden der ersten Seite auf Ihrer SPA-Seite erfolgt. Wenn der Code bei einer Änderung der Ansicht oder bei einer Aktion auf Ihrer Site ausgeführt werden soll, sollten Sie der entsprechenden **[!UICONTROL Regel]** eine zusätzliche Aktion hinzufügen (z. B. beim Laden der Seite: ereignis-Ansicht-End- [!UICONTROL Regel]), sodass der Code jedes Mal ausgeführt wird, wenn die [!UICONTROL Regel] ausgeführt wird. Legen Sie beim Erstellen dieser Aktion in der [!UICONTROL Regel]*Extension = Core* und *Aktionstyp = Benutzerdefinierter Code* fest.

### &quot;Hybrid&quot;-SPA/Reguläre Sites {#hybrid-spa-regular-sites}

Bei einigen Sites handelt es sich um eine Kombination aus &quot;normalen&quot;Seiten und SPA-Seiten. In diesem Fall müssen Sie eine Strategie verwenden, die für beide Seitentypen funktioniert. Achten Sie beim Konfigurieren Ihrer benutzerspezifischen Ereignis auf der Site und beim Auslösen der Regeln [!DNL Experience Platform Launch]darauf, dass keine Dubletten-Treffer von der Seite ausgehen, basierend auf Hash-Änderungen usw. [!DNL Analytics] . (wenn Sie die [!DNL Experience Platform Launch] Regel so auslösen möchten). In diesem Fall müssen Sie eine der Ansichten unterdrücken, damit Sie keine fehlerhaften Daten in Adobe Analytics erhalten.

Wenn Sie die Funktion in separate [!UICONTROL Regeln] unterteilen möchten, damit Sie mehr Kontrolle darüber haben, sollten Sie sich daran erinnern/Dokument, dass Sie dies getan haben, damit alle Änderungen an einer [!UICONTROL Regel] auch an der anderen [!UICONTROL Regel] vorgenommen werden können, um Ihre [!DNL Analytics] Datenintegrität zu schützen.

### Integration mit [!DNL Target] A4T {#integration-with-target-via-a4t}

Nur eine kurze Aufzählung. Wenn Sie mit [!DNL Target] A4T integrieren, stellen Sie sicher, dass die [!DNL Target] Anforderung und die [!DNL Analytics] Anforderung auf derselben Ansicht dieselbe SDID aufweisen. Dadurch wird sichergestellt, dass Ihre Daten ordnungsgemäß mit den Lösungen synchronisiert werden.

Um die Treffer anzuzeigen, verwenden Sie ein Debugger- oder Paket-Sniffer-Programm. Sie können auch den Experience Cloud Debugger, eine Chrome-Erweiterung, die [HIER](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj)heruntergeladen werden können. [!DNL Target] sollte zuerst auf der Seite ausgelöst werden, damit Sie dies auch in der JavaScript-Konsole oder im Debugger überprüfen können.

## Zusätzliche Ressourcen {#additional-resources}

* [SPA-Diskussion in den Foren zur Adobe](https://forums.adobe.com/thread/2451022)
* [Referenzarchitektur-Sites, die zeigen, wie SPA in Experience Platform Launch implementiert wird](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)