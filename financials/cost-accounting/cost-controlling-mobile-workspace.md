---
title: "Mobiler Arbeitsbereich für die Kostensteuerung"
description: "Dieses Thema enthält Informationen zum mobilen Arbeitsbereich Kostensteuerung, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Dieser Arbeitsbereich Kostenstellenmanager zeigt Informationen über die Kostenstellenleistung, jederzeit und überall."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 09383c24b0dd2ad61a836f6c8dc97f4389915772
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Mobiler Arbeitsbereich für die Kostensteuerung

[!include[banner](../includes/banner.md)]


Dieses Thema enthält Informationen zum mobilen Arbeitsbereich Kostensteuerung, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Dieser Arbeitsbereich Kostenstellenmanager zeigt Informationen über die Kostenstellenleistung, jederzeit und überall. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Übersicht über den mobilen Arbeitsbereich Kostensteuerung
-------------------------------------------------

Der Arbeitsbereich **Kostensteuerung** enthält eine einzige Ansicht der Leistung der aktuellen Kostenstellen aus dem Vergleich von Ist-Kosten im Vergleich zu den geplanten Kosten. Sie können den Status einzelner Kostenfaktoren mit Detailinformationen anzeigen. 

Zum Beispiel empfängt ein Mitarbeiter eine Einladung zu einer internationalen Konferenz, aber die Organisation muss alle Reisespesen enthalten. Der Mitarbeiter fragt den Vorgesetzten, ob er an der Konferenz teilnehmen darf. Der Vorgesetzte öffnet schnell den Arbeitsbereich **Kostenkontrolle**auf seinem Mobiltelefon, um festzustellen, ob er das Budget hat, und der Mitarbeiter die Konferenz besuchen kann.

### <a name="data-security"></a>Datensicherheit

Die Daten im mobilen Arbeitsbereich **Kostensteuerung**werden mit Anmeldeinformationen geschützt. Ein Kostenstellenmanager kann nur Daten für seine eigene Kostenstelle sehen. Die Zugriffsebenensicherheit wird im Modul **Kostenrechnung** verwaltet. 

Buchhalter definieren den mobilen Arbeitsbereich **Kostensteuerung** im Modul **Buchhaltungskosten**. Nachdem der Arbeitsbereich auf Microsoft Dynamics 365 For Operations auf der App veröffentlicht ist, ist er in der mobilen App für Dynamics 365 for Operations verfügbar. Dadurch wird sichergestellt, dass alle Kostenstellenmanager in der gleichen Organisation Daten im selben Format sehen.

### <a name="actions-views-and-links"></a>Aktivitäten, Ansichten und Links

Der mobile Arbeitsbereich **Kostensteuerung** in der Dynamics 365 for Operations-App bietet folgende Aktivitäten, Ansichten und Links:

-   **Aktivitäten:**
    -   Verwenden Sie **Konfiguration auswählen**, um ein Layout auszuwählen.
    -   Verwenden Sie **Kostenträger auswählen**, um die Daten auszuwählen, nach denen Kostenstellen gefiltert werden sollen. **Hinweis:** Die Kostenstellen, die in der Liste angezeigt werden, hängen vom Zugriff ab, der im Modul **Kostenrechnung** gewährt wird.
-   **Ansichten:** Auf Grundlage der ausgewählten Aktivitäten und der Konfiguration im Modul **Kostenrechnung** können Sie folgende Informationen in den Karten anzeigen.
    -   Ist-Wert verglichen mit Budget (aktuelle Periode)
    -   Aktuelle Periode vs überarbeitetes Budget (aktuelle Periode)
    -   Ist-Wert verglichen mit Budget (vorherige Periode)
    -   Aktuelle Periode verglichen mit überarbeitetem Budget (vorherige Periode)
    -   Istwert und Budget (seit Jahresbeginn)
    -   Istwert und überarbeitetes Budget (Seit Jahresbeginn)

    Die folgenden Beträge werden für jede Karte angezeigt: Ist-, Budget-, Abweichung und Abweichung %.
-   **Verknüpfungen:**
    -   Details für aktuelle Periode
    -   Details für vorherige Periode
    -   Details für Jahr bis jetzt

    Wenn Sie eine Verknüpfung aktivieren, wird für jeden Ausgaben eine Karte angezeigt. Der Betrag in den Karten wird im folgenden Format angezeigt: Ist, Budget, Planabweichung, Planabweichung %, überarbeitetes Budget, überarbeitetes Budget Abweichung und überarbeitete Budget Abweichung %. 
    
    [![Karte für ein Kostenelement](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Voraussetzungen
Bevor Sie den mobilen Arbeitsbereich **Kostensteuerung** verwenden können, überprüfen Sie, ob Ihr Systemadministrator die folgenden Voraussetzungen bereitgestellt hat.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder späterem muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>Wenn Sie nicht bereits Dynamics 365 for Operations in Ihrer Organisation bereitgestellt haben, sollte Ihr Systemadministrator <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations Testumgebung bereitstellen</a> sehen.</td>
</tr>
<tr class="even">
<td>4013633 KB muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>KB 4013633 (eine X++-Aktualisierung oder ein Metadatenhotfix) enthält vier mobile Arbeitsbereiche für die Lieferkettenverwaltung. Um KB 4013633 zu implementieren, muss Ihr Systemadministrator folgende Schritte ausführen:
<ol>
<li>Herunterladen von KB 4013633 von Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Anwenden eines Bereitstellungspaket</a> auf einem Microsoft Dynamics 365 for Operations-System</li>
</ol></td>
</tr>
<tr class="odd">
<td>Der mobile Arbeitsbereich <strong>Kostensteuerung</strong> muss in der Dynamics 365 for Operations Mobile App veröffentlicht sein.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Starten Sie Dynamics 365 for Operations in Ihrem Browser.</li>
<li>Wählen Sie <strong>Mobile Arbeitsbereiche verwalten</strong> auf der <strong>Systemparameter</strong> Seite aus.</li>
<li>Wählen Sie den Arbeitsbereich <strong>Kostenträgerüberblick</strong> aus.</li>
<li>Klicken Sie auf <strong>Mobilen Arbeitsbereich veröffentlichen</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laden Sie Dynamics 365 for Operations mobile App herunter und installieren Sie diese.
Laden Sie die App im App Store herunter und installieren Sie die Microsoft Dynamics 365 for Operations-App.

-   Für Android - [Dynamics 365 for Operations im Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Für iPhone: [Dynamics 365 for Operations im iTunes-App-Store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Melden Sie sich an und nutzen Sie Dynamics 365 for Operations mobile App.
1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die Dynamics 365 for Operations URL ein.
3.  Geben Sie das Unternehmen ein. Geben Sie beispielsweise **USMF** ein.
4.  Wenn Sie sich zum ersten Mal anmelden, werden Sie nach einem Benutzernamen und einem Kennwort für Ihr Microsoft Dynamics 365 for Operations Konto gefragt. Geben Sie Ihre Anmeldeinformationen ein.
5.  Nachdem Sie sich angemeldet haben, sehen Sie verfügbaren Arbeitsbereiche für Ihr Unternehmen. Beachten Sie, dass, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, Sie die Liste der Arbeitsbereiche aktualisieren müssen. 

    [![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Hier können Sie die Leistungsfähigkeit der Kostenstellen sehen, indem Sie den mobilen Arbeitsbereich Kostensteuerung verwenden
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Kostensteuerung**.
2.  Wählen Sie **Kostenträgersteuerung**.
3.  Wählen Sie **Aktivitäten**.
4.  Klicken Sie auf **Konfiguration auswählen**, um das Layout der Kostensteuerung zu wählen.
5.  Wählen Sie **Fertig**.
6.  Wählen Sie **Aktivitäten**.
7.  Klicken Sie auf **Kostenträger auswählen**, um die Kostenstelle auszuwählen, auf die Sie Zugriff haben.
8.  Wählen Sie **Fertig**.
9.  Hier können Sie die Leistung der Kostenstelle anzeigen.
10. Wählen Sie den Link aus **Details für aktuelle Periode**.
11. Hier können Sie die Leistung der einzelnen Kostenelemente anzeigen
12. Sie können auch nach bestimmten Kostenfaktoren suchen.





