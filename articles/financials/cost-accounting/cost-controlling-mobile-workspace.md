---
title: "Mobiler Arbeitsbereich für die Kostensteuerung"
description: "Dieses Thema enthält Informationen zur Kostensteuerung im mobilen Arbeitsbereich. Dieser Arbeitsbereich Kostenstellenmanager zeigt Informationen über die Kostenstellenleistung, jederzeit und überall."
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 5b57bf268ac9e91c98a0b8709061e695ebf482c6
ms.contentlocale: de-de
ms.lasthandoff: 12/01/2017

---

# <a name="cost-controlling-mobile-workspace"></a>Mobiler Arbeitsbereich für die Kostensteuerung

[!include[banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur **Kostensteuerung** im mobilen Arbeitsbereich. Dieser Arbeitsbereich Kostenstellenmanager zeigt Informationen über die Kostenstellenleistung, jederzeit und überall.

Dieser mobile Arbeitsbereich soll mit der Mobil-App für Microsoft Dynamics 365 für Unified Operations verwendet werden.

## <a name="overview"></a>Überblick
Der Arbeitsbereich **Kostensteuerung** enthält eine einzige Ansicht der Leistung der aktuellen Kostenstellen aus dem Vergleich von Ist-Kosten im Vergleich zu den geplanten Kosten. Sie können den Status einzelner Kostenelemente mit Detailinformationen anzeigen.

Zum Beispiel empfängt ein Mitarbeiter eine Einladung zu einer internationalen Konferenz, aber die Organisation muss alle Reisespesen enthalten. Der Mitarbeiter fragt den Vorgesetzten, ob er an der Konferenz teilnehmen darf. Der Vorgesetzte öffnet schnell den Arbeitsbereich **Kostenkontrolle** auf seinem Mobiltelefon, um festzustellen, ob er das Budget hat, und der Mitarbeiter die Konferenz besuchen kann.

### <a name="data-security"></a>Datensicherheit
Die Daten im mobilen Arbeitsbereich **Kostensteuerung** werden mit Anmeldeinformationen geschützt. Ein Kostenstellenmanager kann nur Daten für seine eigene Kostenstelle sehen. Die Zugriffsebenensicherheit wird im Modul **Kostenrechnung** verwaltet.

Buchhalter definieren den mobilen Arbeitsbereich **Kostensteuerung** im Modul **Buchhaltungskosten**. Nachdem der Arbeitsbereich auf der App veröffentlicht ist, ist er in der mobilen App für Dynamics 365 for Operations verfügbar. Dadurch wird sichergestellt, dass alle Kostenstellenmanager in der gleichen Organisation Daten im selben Format sehen.

### <a name="actions-views-and-links"></a>Aktivitäten, Ansichten und Links
Der mobile Arbeitsbereich **Kostensteuerung** bietet folgende Aktivitäten, Ansichten und Links:

-   **Aktivitäten:**

    -   Verwenden Sie **Konfiguration auswählen**, um ein Layout auszuwählen.
    -   Verwenden Sie **Kostenträger auswählen**, um die Daten auszuwählen, nach denen Kostenstellen gefiltert werden sollen.
    
        > [!NOTE]
        > Die Kostenstellen, die in der Liste angezeigt werden, hängen vom Zugriff ab, der im Modul **Kostenrechnung** gewährt wird.

-   **Ansichten:** Auf Grundlage der ausgewählten Aktivitäten und der Konfiguration im Modul **Kostenrechnung** können Sie folgende Informationen in den Karten anzeigen:

    -   Ist-Wert verglichen mit Budget (aktuelle Periode)
    -   Ist-Wert verglichen mit überarbeitetem Budget (aktuelle Periode)
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
    
    [![Karte für ein Kostenelement](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen unterscheiden sich basierend auf der Version von Microsoft Dynamics 365, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition verwenden
Wenn Microsoft Dynamics 365 for Finance and Operations, Enterprise edition für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Kostensteuerung** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später verwenden.
Wenn Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen.

<table>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementieren Sie KB 4013633.</td>
<td>Systemadministrator</td>

<td>KB 4013633 ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Kostensteuerung</strong> enthält. Um KB 4013633 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laden Sie den Metadatenhotfix für Microsoft Dynamics Lifecycle Services (LCS) herunter</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Das bereitstellbare Paket übernehmen</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Den mobilen Arbeitsbereich <strong>Kostensteuerung</strong> veröffentlichen.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App
Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:

-   [Für Androide-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die URL Dynamics 365 ein.
3.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
4.  Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

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


