---
title: 'Verwenden von Best Practices beim Tracking von Single Page Applications (SPA) in Adobe Analytics '
description: In diesem Dokument beschreiben wir verschiedene Best Practices, die Sie befolgen und kennen sollten, wenn Sie Adobe Analytics zum Tracking von Single Page Applications (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung von Experience Platform Launch, was die empfohlene Implementierungsmethode ist.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: ht
source-wordcount: '1669'
ht-degree: 100%

---

# Verwenden von Best Practices beim Tracking von Single Page Applications (SPA) in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In diesem Dokument beschreiben wir verschiedene Best Practices, die Sie befolgen und kennen sollten, wenn Sie Adobe Analytics zum Tracking von Single Page Applications (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung von Adobe [!DNL Experience Platform Launch], was die empfohlene Implementierungsmethode ist.

VORABBEMERKUNGEN:

* Bei den folgenden Elementen wird davon ausgegangen, dass Sie [!DNL Experience Platform Launch] zur Implementierung auf Ihrer Site verwenden. Wenn Sie [!DNL Experience Platform Launch] nicht verwenden, gelten die Überlegungen trotzdem, Sie müssen sie jedoch an Ihre Implementierungsmethode anpassen.
* Alle SPAs sind unterschiedlich, sodass Sie möglicherweise einige der folgenden Elemente anpassen müssen, damit sie bestmöglich auf Ihre Anforderungen passen. Dennoch wollten wir einige Best Practices mit Ihnen teilen – Dinge, über die Sie bei der Implementierung von Adobe Analytics auf SPA-Seiten nachdenken müssen.

## Einfaches Diagramm zum Arbeiten mit SPAs in [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![SPA für Analysen in Launch](assets/spa_for_analyticsinlaunch.png)

**HINWEIS:** Wie angegeben, ist dies ein vereinfachtes Diagramm dazu, wie SPA-Seiten in einer Adobe Analytics-Implementierung mit [!DNL Experience Platform Launch] gehandhabt werden. In den folgenden Abschnitten dieser Seite erläutern wir die Schritte und Probleme, die Sie sorgfältig überdenken bzw. bei denen Sie Maßnahmen ergreifen sollten.

## Definieren der Datenschicht {#setting-the-data-layer}

Wenn neuer Inhalt auf einer SPA-geladen wird oder wenn eine Aktion auf einer SPA-Seite stattfindet, sollten Sie als Erstes die Datenschicht aktualisieren. Dies muss geschehen, BEVOR das benutzerspezifische Ereignis eintritt und als Trigger für Regeln in [!DNL Experience Platform Launch] fungiert, sodass [!DNL Experience Platform Launch] die neuen Werte aus der Datenschicht übernehmen und in Adobe Analytics übertragen kann.

Im Folgenden finden Sie eine Beispieldatenschicht, deren Elemente bei Änderung der Ansicht oder Aktion in Ihrer SPA geändert werden können. Bei einer vollständigen/mehrheitlichen Bildschirmänderung wäre es beispielsweise üblich, ein [!DNL pageName]-Element zu ändern, damit das neue Element in [!DNL Experience Platform Launch] erfasst und an Adobe Analytics gesendet werden kann.

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

## Festlegen benutzerspezifischer Ereignisse und Listening-Ereignisse in [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Wenn neuer Inhalt auf der Seite geladen wird oder eine Aktion auf der Site stattfindet, sollten Sie [!DNL Experience Platform Launch] darüber in Kenntnis setzen, damit eine Regel ausgeführt und Daten an [!DNL Analytics] gesendet werden können. Dazu gibt es verschiedene Möglichkeiten: [!UICONTROL Direktaufruf]-[!UICONTROL Regeln] oder benutzerspezifische Ereignisse.

* [!UICONTROL Direktaufruf]-[!UICONTROL Regeln]: In [!DNL Experience Platform Launch] können Sie eine [!UICONTROL Direktaufruf]-[!UICONTROL Regel] einrichten, die ausgeführt wird, wenn sie direkt von der Seite aus aufgerufen wird. Wenn das Laden Ihrer Seite oder Ihre Aktion auf Ihrer Site sehr einfach ist oder wenn sie eindeutig ist und jedes Mal einen bestimmten Satz von Anweisungen ausführen kann (definieren Sie [!DNL eVar4] als X und lösen Sie jedes Mal [!DNL event2] aus), können Sie eine [!UICONTROL Direktaufruf]-[!UICONTROL Regel] verwenden. Weitere Informationen zum Erstellen von [!UICONTROL Direktaufruf]-[!UICONTROL Regeln] finden Sie in der [!DNL Experience Platform Launch]-Dokumentation.
* Benutzerspezifische Ereignisse: Für mehr Funktionalität und für die Möglichkeit, eine Payload mit unterschiedlichen Werten dynamisch anzuhängen, sollten Sie benutzerdefinierte JavaScript-Ereignisse festlegen und diese mit [!DNL Experience Platform Launch] im Blick behalten. Dort können Se die Payload verwenden, um Variablen festzulegen und die Daten an Adobe Analytics zu senden. Es ist wahrscheinlicher, dass Sie diese Funktion benötigen. Daher gilt diese Option als Best Practice. Jede Funktion auf Ihrer Site kann jedoch bestimmen, welche Methode am besten geeignet ist. Wir werden in diesem Dokument unter der Annahme fortfahren, dass Sie diese benutzerspezifische Ereignismethode verwenden.

**Beispiele:** In [DIESEM](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html?lang=de) Hilfedokument gibt es Links zu Beispiel-SPA-Sites, auf denen [!DNL Analytics] (und anderen Experience Cloud-Lösungen) implementiert sind, sowie Unterlagen, die beschreiben, was implementiert wurde. In diesen SPA-Beispielen wurden die folgenden benutzerdefinierten Ereignisse verwendet:

* [!DNL event-view-start]: Dieses Ereignis sollte beim Ansichtsbeginn der Ansicht/des Status ausgelöst werden, die bzw. der geladen wird.
* [!DNL event-view-end]: Dieses Ereignis sollte auch dann ausgelöst werden, wenn eine Ansicht-/Statusänderung stattgefunden hat und alle SPA-Komponenten auf der Seite vollständig geladen wurden. Dies ist das Ereignis, bei dem normalerweise ein Aufruf an Adobe Analytics getriggert wird.
* [!DNL event-action-trigger]: Dieses Ereignis sollte ausgelöst werden, wenn ein beliebiges Ereignis auf der Seite auftritt, mit Ausnahme des Ladevorgangs von Ansicht/Status. Dies kann ein Klickereignis oder eine kleinere Inhaltsänderung ohne Änderung der Ansicht sein.

Weitere Informationen dazu, wie/wann diese Ereignisse ausgelöst werden, finden Sie auf bzw. in den oben referenzierten Seiten/Dokumenten. Sie müssen nicht dieselben Ereignisnamen verwenden, aber die hier aufgeführten Funktionen sind empfohlene Best Practices. Im folgenden Video wird eine Beispiel-Site gezeigt und auch, wo in [!DNL Experience Platform Launch] auf die benutzerdefinierten Ereignisse gewartet werden sollte.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ausführen von „s.t()“ oder „s.tl()“ in der [!DNL Experience Platform Launch]-[!UICONTROL Regel] {#running-s-t-or-s-tl-in-the-launch-rule}

Eines der wichtigsten Dinge, die es bei der Arbeit mit einer SPA im Hinblick auf [!DNL Analytics] zu verstehen gilt, ist der Unterschied zwischen `s.t()` und `s.tl()`. Sie werden eine dieser Methoden in [!DNL Experience Platform Launch] zum Senden von Daten an [!DNL Analytics] auslösen, aber Sie müssen wissen, wann die jeweilige Methode gesendet wird.

* **s.t()**: „t“ steht für „track“ (nachverfolgen) und ist eine normale Seitenansicht. Auch wenn sich die URL möglicherweise nicht ändert, ändert sich die Ansicht so, dass Sie sie als neue „Seite“ *betrachten* würden? Wenn ja, legen Sie die Variable „s.[!DNL pageName]“ fest und verwenden Sie `s.t()`, um den Aufruf an [!DNL Analytics] zu senden.

* **s.tl()**: „tl“ steht für „track link“ (Link nachverfolgen) und wird normalerweise zum Tracking von Klicks oder kleinen Inhaltsänderungen m Gegensatz zu einer kompletten Änderung der Anzeige verwendet. Wenn die Änderung auf Ihrer Seite nur klein ist, sodass Sie sie nicht als vollständige neue „Seite“ betrachten, verwenden Sie `s.tl()` und sparen Sie sich den Aufwand, die Variable s.pageName festzulegen, denn [!DNL Analytics] wird sie ignorieren.

**TIPP:** Einige Benutzer verwenden eine allgemeine Regel, wonach der Bildschirm, wenn er sich um mehr als 50 % ändert, als Seitenansicht betrachtet und `s.t()` verwendet werden sollte. Wenn die Änderung am Bildschirm weniger als 50 % beträgt, verwenden Sie `s.tl()`. Es liegt jedoch ganz bei Ihnen, was Sie als neue „Seite“ betrachten und wie Sie Ihre Site in Adobe Analytics nachverfolgen möchten.

Im folgenden Video wird gezeigt, wo und wie Sie in Experience Platform Launch `s.t()` oder `s.tl()` auslösen lassen können.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Löschen von Variablen {#clearing-variables}

Wenn Sie Ihre Site mit Adobe Analytics nachverfolgen, möchten Sie natürlich nur die richtigen Daten zum richtigen Zeitpunkt an [!DNL Analytics] senden. In einer SPA-Umgebung kann ein in einer [!DNL Analytics]-Variable verfolgter Wert bestehen bleiben und erneut an [!DNL Analytics] gesendet werden, möglicherweise auch dann, wenn wir dies nicht mehr wünschen. Aus diesem Grund gibt es eine Funktion in der [!DNL Launch]-Erweiterung von [!DNL Analytics], um die Variablen zu löschen, sodass Sie bei der nächsten Bildanforderung und beim Senden von Daten in [!DNL Analytics] einen neuen Anfang machen können.

Im obigen Diagramm ist sie am Ende des Prozesses aufgeführt und löscht die Variablen, *nachdem* Sie den Treffer gesendet haben. In Wirklichkeit kann dies entweder vor ODER nach dem Absenden des Treffers geschehen, aber Sie sollten in Ihren [!DNL Experience Platform Launch]-Regeln konsequent sein, sodass das Löschen immer entweder vor oder nach dem Setzen der Variablen und dem Absenden erfolgt. Denken Sie daran: Wenn Sie die Variablen löschen möchten, *bevor* Sie `s.t()` ausführen, stellen Sie sicher, dass Sie zuerst die Variablen löschen, dann die neuen Variablen setzen und schließlich die neuen Daten an [!DNL Analytics] senden.

**HINWEIS:** Das Löschen von Variablen ist nicht immer erforderlich, wenn `s.tl()` ausgeführt wird, da `s.tl()` jedes Mal die Verwendung der [!DNL linkTrackVars]-Variable erfordert, um [!DNL Analytics] mitzuteilen, welche Variablen gesetzt werden sollen (wird automatisch hinter den Kulissen in [!DNL Experience Platform Launch] hinzugefügt). Das bedeutet, dass fehlerhafte Variablen bei der Verwendung von `s.tl()` normalerweise nicht auftauchen, aber es wird sehr empfohlen, wenn `s.t()` in einer SPA-Umgebung verwendet wird. Dennoch möchte ich empfehlen, in einer SPA-Umgebung die Funktion „Variablen löschen“ sowohl für `s.t()` als auch für `s.tl()` zu verwenden, um eine qualitativ hochwertige Datenerfassung zu gewährleisten.

Das folgende Video zeigt, wo und wie die Variablen in [!DNL Launch] gelöscht werden können.

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Weitere zu berücksichtigende Aspekte {#additional-considerations}

### Fenster mit benutzerspezifischem Code in [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

In der [!DNL Analytics]-Erweiterung von [!DNL Launch] gibt es zwei Stellen, an denen Sie benutzerdefinierten Code einfügen können: im Abschnitt [!UICONTROL Bibliotheksverwaltung] und im zusätzlichen Abschnitt [!UICONTROL Tracker mit benutzerdefiniertem Code konfigurieren].

![Starten von benutzerdefinierten Code-Fenstern in Analytics](assets/launch_analyticscustomcodewindows.png)

Es ist wichtig zu wissen, dass der Code an diesen beiden Stellen nur einmal ausgeführt wird, nämlich beim ersten Laden der SPA-Seite. Wenn der Code bei einem Wechsel der Ansicht oder bei einer Aktion auf Ihrer Seite ausgeführt werden soll, sollten Sie eine zusätzliche Aktion zu der entsprechenden **[!UICONTROL Regel]** hinzufügen (z. B. in der [!UICONTROL Regel] „page load: event-view-end“), sodass der Code jedes Mal ausgeführt wird, wenn die [!UICONTROL Regel] läuft. Wenn Sie diese Aktion in der [!UICONTROL Regel] erstellen, setzen Sie *Extension = Core* und *Action Type = Custom Code*.

### „Hybride“ SPA-/reguläre Sites {#hybrid-spa-regular-sites}

Einige Websites sind eine Kombination aus „regulären“ Seiten und SPA-Seiten. In diesem Fall müssen Sie eine Strategie verwenden, die für beide Seitentypen funktioniert. Wenn Sie Ihre benutzerdefinierten Ereignisse auf der Website konfigurieren und die Regeln in [!DNL Experience Platform Launch] ausgelöst werden, achten Sie darauf, dass es keine doppelten Treffer gibt, die von der Seite aus in [!DNL Analytics] eingehen, basierend auf Hash-Änderungen usw. (falls Sie die [!DNL Experience Platform Launch]-Regel auf diese Weise auslösen wollen). In diesem Fall müssen Sie eine der Seitenansichten unterdrücken, damit Sie keine fehlerhaften Daten in Adobe Analytics erhalten.

Wenn Sie sich entscheiden, die Funktionalität in separate [!UICONTROL Regeln] aufzuteilen, um mehr Kontrolle darüber zu haben, stellen Sie sicher, dass Sie sich daran erinnern bzw. dokumentieren, dass Sie dies getan haben, damit alle Änderungen an einer [!UICONTROL Regel] auch an der anderen [!UICONTROL Regel] vorgenommen werden können, um die Integrität Ihrer [!DNL Analytics]-Daten zu schützen.

### Integration mit [!DNL Target] über A4T {#integration-with-target-via-a4t}

Nur ein kurzer Hinweis. Wenn Sie [!DNL Target] mit A4T integrieren, stellen Sie sicher, dass die [!DNL Target]-Anfrage und die [!DNL Analytics]-Anfrage bei der gleichen Ansichtsänderung die gleiche SDID haben. Dadurch wird sichergestellt, dass Ihre Daten ordnungsgemäß mit den Lösungen synchronisiert werden.

Um die Treffer anzuzeigen, verwenden Sie ein Debugger- oder Paket-Sniffer-Programm. Sie können auch den Experience Cloud Debugger verwenden, eine Chrome-Erweiterung, die [HIER](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) heruntergeladen werden kann. [!DNL Target] sollte zuerst auf der Seite ausgelöst werden, damit Sie dies auch in der JavaScript-Konsole oder im Debugger überprüfen können.

## Zusätzliche Ressourcen {#additional-resources}

* [SPA in den Adobe-Foren](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940?profile.language=de)
* [Referenz-Sites zur Architektur, die zeigen, wie SPA in Experience Platform Launch implementiert wird](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html?lang=de)
