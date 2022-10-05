---
title: Best Practices für die Implementierung von Einzelseiten-Apps (SPA)
description: Erfahren Sie mehr über Best Practices zur Implementierung von Adobe Analytics in Einzelseiten-Apps (SPA). Dazu gehört die Verwendung von Experience Platform Tags, der empfohlenen Implementierungsmethode.
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
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 3%

---

# Best Practices für die Implementierung von Einzelseiten-Apps (SPA) {#implementation-best-practices-for-single-page-appliations}

Erfahren Sie mehr über die Best Practices zur Implementierung von [!DNL Adobe Analytics] auf Einzelseiten-Apps (SPA). Dazu gehört die Verwendung von [!DNL Experience Platform Tags], die empfohlene Implementierungsmethode.

VORABBEMERKUNGEN:

* Der folgende Inhalt verweist auf die Verwendung von [!DNL Experience Platform Tags] , um Adobe Analytics auf Ihrer Site zu implementieren. Diese Überlegungen gelten, wenn [!DNL Experience Platform Tags] nicht verwendet wird, müssen Sie sie daher an Ihre Implementierungsmethode anpassen.
* Es gibt Unterschiede in SPA. Daher sollten Sie Ihren Ansatz entsprechend Ihren Bedürfnissen anpassen.

## Einfaches Diagramm zum Arbeiten mit SPAs in [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA für Analysen in Tags](assets/spa_for_analyticsinlaunch.png)

**HINWEIS:** Dies ist ein vereinfachtes Diagramm zur Handhabung SPA Seiten in einer Adobe Analytics-Implementierung mit [!DNL Experience Platform Tags]. In den folgenden Abschnitten werden die zu berücksichtigenden Schritte und Probleme beschrieben.

## Datenschicht festlegen {#set-the-data-layer}

Wenn neuer Inhalt geladen wird oder eine Aktion auf einer SPA erfolgt, *Aktualisieren der Datenschicht zuerst*. Das muss geschehen **before** ein benutzerspezifisches Ereignis, bei dem eine Regel in Trigger ausgeführt wird [!DNL Experience Platform Tags]. Dadurch wird sichergestellt, dass die richtigen Werte aus der Datenschicht in Tags und dann in Adobe Analytics übertragen werden.

Im Folgenden finden Sie eine Beispieldatenschicht. Jedes dieser Elemente kann sich basierend auf der anfänglichen Ansicht oder der nachfolgenden Änderung der Ansicht ändern, wenn eine auf Ihrer SPA durchgeführte Aktion durchgeführt wird. Bei einer Änderung der vollständigen oder mehrheitlichen Ansicht ist es beispielsweise üblich, eine eindeutige[!DNL pageName]&quot;, um zwischen den Ansichten in Adobe Analytics-Berichten zu unterscheiden.

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

## Festlegen benutzerdefinierter Ereignisse und Überwachen dieser Ereignisse in [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Wenn neue Inhalte geladen werden oder eine Aktion auf der SPA erfolgt, müssen Experience Platform-Tags informiert werden, um eine Regel auszuführen, die Daten an sendet [!DNL Analytics]. Dazu gibt es mehrere Ansätze: [!UICONTROL Direktaufrufregeln] oder benutzerspezifische Ereignisse.

* [!UICONTROL Direktaufrufregeln]: Richten Sie eine [!UICONTROL Direktaufrufregel] wird ausgeführt, wenn sie direkt von der Seite aus aufgerufen wird. Wenn das Laden oder die Aktion der Seite einfach oder eindeutig ist und einen bestimmten Satz von Anweisungen jedes Mal ausführen kann (z. B. [!DNL eVar4] nach X und Trigger [!DNL event2] jedes Mal), ist dieser Ansatz geeignet. Siehe [!DNL Experience Platform Tags] Dokumentation für weitere Informationen zum Erstellen [!UICONTROL Direktaufrufregeln].
* Benutzerspezifische Ereignisse: Wenn Sie eine Payload mit eindeutigen Werten für Ereignisse, die auf SPA Seiten auftreten, dynamisch anhängen müssen, verwenden Sie benutzerdefinierte JavaScript-Ereignisse und überwachen Sie sie in [!DNL Experience Platform Tags]. Verwenden Sie die Payload, um Datenelemente und Analytics-Variablen in Tags festzulegen. Diese Methode wird als Best Practice betrachtet, da diese Anforderung normalerweise für SPA gilt. In unseren Beispielen unten wird die Methode für benutzerspezifische Ereignisse verwendet.

**Beispiele:** [In diesem](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) Hilfedokument: Es gibt Links zu Beispiel-SPA-Sites, die implementieren [!DNL Analytics] und anderen Experience Cloud-Lösungen. In diesen Beispielen werden die folgenden benutzerdefinierten Ereignisse verwendet:

* **[!DNL Event-view-start]**: Wird am Ansichtsbeginn der Ansicht/des Status ausgeführt, die geladen wird.
* **[!DNL Event-view-end]**: Wird ausgeführt, wenn eine Ansicht-/Statusänderung erfolgt und alle SPA Komponenten auf der Seite vollständig geladen werden. Dies ist das Ereignis, das normalerweise Daten an Adobe Analytics sendet.
* **[!DNL Event-action-trigger]**: Wird ausgeführt, wenn ein Ereignis auf der Seite auftritt, mit Ausnahme des Ladevorgangs von Ansicht/Status. Beispiele dafür sind ein Klickereignis oder eine kleinere Inhaltsänderung ohne Änderung der Ansicht.

Weitere Informationen dazu, wie und wann diese Ereignisse ausgelöst werden, finden Sie auf den oben genannten Seiten und Dokumenten. Sie müssen nicht dieselben Ereignisnamen in Ihrer Implementierung verwenden. Der funktionale Anwendungsfall für die verwendete Methode ist unerlässlich, um als empfohlene Best Practice für jede Methode zu verstehen. Das folgende Video zeigt eine SPA und einen Beispielcode in [!DNL Experience Platform Tags] , der auf die benutzerdefinierten Ereignisse überwacht.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Führen Sie s.t() oder s.tl() im [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Ein wichtiges Konzept für [!DNL Analytics] beim Arbeiten mit einem SPA ist der Unterschied zwischen `s.t()` und `s.tl()`. Ihr Code Trigger eine dieser Methoden in [!DNL Experience Platform Tags] zum Senden von Daten an [!DNL Analytics].

* **s.t()** - &quot;t&quot;steht für &quot;track&quot;, und dies stellt eine Seitenansicht dar. Wenn sich die Ansicht so ändert, dass Sie  *erwägen* eine neue &quot;Seite&quot;verwenden, verwenden Sie diesen Aufruf. Legen Sie einen eindeutigen Wert für [!DNL s.pageName] Variablen und Verwendung `s.t()` , um die Daten an [!DNL Analytics].

* **s.tl()** - &quot;tl&quot;steht für &quot;track link&quot;, was einen Link-Klick oder eine kleine Inhaltsänderung darstellt. Wenn die Änderung der Ansicht minimal ist, verwenden Sie `s.tl()` , um einen eindeutigen Wert über die Interaktion an [!DNL Analytics]. Diese übergebene Variable ist nicht [!DNL s.pageName], da dies in Analytics ignoriert wird, wenn `s.tl()` -Aufrufe empfangen werden.

**TIPP:** Wenn sich der Bildschirm als allgemeine Richtlinie um mehr als 50 % ändert, verwenden Sie die `s.t()` Seitenansichtsaufruf. Verwenden Sie andernfalls `s.tl()`. Verwenden Sie Ihr Urteilsvermögen jedoch bei der Erwägung von Aktionen, die eine neue &quot;Seite&quot;darstellen, und wie dies in Adobe Analytics-Berichten dargestellt werden sollte.

Im folgenden Video wird gezeigt, wo und wie Trigger `s.t()` oder `s.tl()` in Tags.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Variablen löschen {#clear-variables}

Senden Sie die richtigen Daten an [!DNL Analytics] zum richtigen Zeitpunkt. In einer SPA-Umgebung wird ein Wert gespeichert in einer [!DNL Analytics] bleibt bestehen und wird erneut in [!DNL Analytics], wenn Sie sie nicht mehr benötigen. Eine Funktion ist in der Variablen [!DNL Analytics] [!DNL Tags] Erweiterung, um die Variablen zu löschen und sicherzustellen, dass beim nächsten Aufruf keine Daten fälschlicherweise an gesendet werden [!DNL Analytics].

Das obige Diagramm zeigt die gelöschten Variablen *after* Daten senden. In der Realität kann dies vor ODER nach dem -Aufruf geschehen, jedoch in Ihrer [!DNL Experience Platform Tags] Regeln für eine sauberere Implementierung. Wenn Sie Variablen löschen *before* ausführen `s.t()`, legen Sie die neuen Variablen unmittelbar nach dem Aufruf fest und fahren Sie dann mit dem Senden der neuen Daten an fort. [!DNL Analytics].

**HINWEIS:** Das Löschen von Variablen ist beim Ausführen nicht immer erforderlich `s.tl()`. Dieser Aufruf erfordert die Verwendung der [!DNL linkTrackVars] -Variable anzuweisen [!DNL Analytics] welche Variablen festgelegt werden. Dies geschieht automatisch [!DNL Experience Platform Tags] durch Konfiguration. Dadurch wird verhindert, dass fehlerhafte Variablen im Gegensatz zum Verhalten mit `s.t()` -Aufrufe in einer SPA Umgebung. Um eine sauberste und zuverlässigste Implementierung sicherzustellen, ist es wahrscheinlich einfacher, die Funktion &quot;clear variables&quot;für beide Aufrufe in einer SPA-Umgebung zu verwenden.

Das folgende Video zeigt, wo und wie Variablen in gelöscht werden [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Weitere Überlegungen {#additional-considerations}

### Fenster für benutzerdefinierten Code in [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

Im [!DNL Tags] [!DNL Analytics] -Erweiterung verwenden, können an zwei Stellen benutzerspezifischen Code eingefügt werden: Die &quot;[!UICONTROL Bibliotheksverwaltung]&quot; und &quot;[!UICONTROL Konfigurieren des Trackers mit benutzerdefiniertem Code]&quot;.

![Tags Benutzerdefinierte Codefenster für Analytics](assets/launch_analyticscustomcodewindows.png)

Einer dieser Speicherorte führt den darin enthaltenen Code einmal für die erste Seite aus, an der Ihre SPA geladen wird. Wenn der Code bei einer Ansicht- oder Aktionsänderung ausgeführt werden soll, implementieren Sie diesen Code in der entsprechenden **[!UICONTROL Regel]** (z. B. das Laden der Seite: Regel &quot;event-view-end&quot;), um sicherzustellen, dass der Code jedes Mal ausgeführt wird, wenn die [!UICONTROL Regel] läuft. Beim Erstellen dieser Aktion im [!UICONTROL Regel], set *Erweiterung = Core* und *Aktionstyp = benutzerspezifischer Code*.

### &quot;Hybride SPA und traditionelle Sites&quot; {#hybrid-spa-and-traditional-sites}

Einige Websites bestehen aus einer Kombination aus traditionellen und SPA Seiten. Verwenden Sie in diesem Fall eine Strategie, die für beide Seitentypen funktioniert. Beim Konfigurieren Ihrer benutzerspezifischen Ereignisse auf der Site und Auslösen von Regeln in [!DNL Experience Platform Tags]stellen Sie sicher, dass keine doppelten Treffer an gesendet werden. [!DNL Analytics] basierend auf Hash-Änderungen usw. Unterdrücken Sie in diesem Fall eine der Seitenansichten, um zu verhindern, dass doppelte Daten an Adobe Analytics übergeben werden.

Wenn Sie die Funktion in eindeutige [!UICONTROL Regeln] für mehr Kontrolle dokumentieren, dass Sie dies getan haben. Wenn Sie eine [!UICONTROL Regel], nehmen Sie die gleiche Änderung an der anderen vor [!UICONTROL Regel].

### Integration mit [!DNL Target] Verwendung von A4T {#integration-with-target-using-a4t}

Bei der Integration in [!DNL Target] Überprüfen Sie mithilfe von A4T, ob die Variable [!DNL Target] und [!DNL Analytics] -Anfragen, die in derselben Ansicht oder Aktion gesendet werden, übergeben denselben SDID-Parameterwert. Dadurch wird sichergestellt, dass Ihre Daten im Backend ordnungsgemäß synchronisiert werden.

Verwenden Sie ein Debugger- oder Paketüberwachungstool, um diese Treffer anzuzeigen. Adobe bietet zu diesem Zweck einen Experience Platform Debugger. Es handelt sich um eine Chrome-Erweiterung, die [heruntergeladen hier](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=de). [!DNL Target] zuerst auf der Seite ausgeführt werden. Dies kann auch im Debugger überprüft werden.

## Zusätzliche Ressourcen {#additional-resources}

* [SPA in den Adobe-Foren](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940)
* [Referenz-Sites zur Architektur, die zeigen, wie SPA in Experience Platform Launch implementiert wird](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
