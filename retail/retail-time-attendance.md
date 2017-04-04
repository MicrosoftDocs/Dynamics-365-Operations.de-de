---
title: Zeit und Anwesenheit im Einzelhandel
description: "In diesem Thema werden die möglichen Szenarien, die für Aufwandsprojekte Anwesenheitsverwaltung in Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge unterstützt werden."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Zeit und Anwesenheit im Einzelhandel

In diesem Thema werden die möglichen Szenarien, die für Aufwandsprojekte Anwesenheitsverwaltung in Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge unterstützt werden. 

<a name="manage-worker-setup-and-scheduling"></a>Verwalten Sie Arbeitskrafteinstellung und Feinterminierung
----------------------------------

### <a name="initial-configuration"></a>Ausgangskonfiguration

-   Führen Sie den Konfigurationsassistenten aus.
-   Registrieren Sie Arbeitskräfte als Zeiterfassungsarbeitskräfte.

### <a name="plan-worker-schedules"></a>Planen von Arbeitskraftzeitplänen

-   Wenden Sie Profile durch Verwendung der Arbeitsplanung an. Weitere Informationen finden Sie unter <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Informationen zu den Konfigurationsschritten finden Sie unter <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Einzelhandelsspezifische Konfiguration

-   Aktivieren Sie ein Funktionsprofil für die Zeiterfassung für Arbeitskräfte, für die Sie Zeiterfassungen aktivieren möchten. ** Auf POS-Funktionsprofilen ** &gt; ** Funktionen ** &gt; ** POS-Zeiterfassungen ** &gt; ** aktivieren Sie Zeiterfassungen **.
-   Konfigurieren Sie Point-of-Sale-Berechtigungsgruppen (POS), um die Berechtigung zum Anzeigen von Zeiterfassungseinträgen zu aktivieren. Diese Berechtigung ermöglicht einem Benutzer die Anzeige der Zeiterfassungen anderer Arbeitskräfte im Shop (und von jedem anderen Shops, dem der Benutzer zugeordnet ist, über das Adressbuch). Sie sollten diese Berechtigung für eine Managerrolle aber nicht für eine Kassiererrolle aktivieren. ** Auf POS-Berechtigungsgruppen ** &gt; ** zeigen Sie Stempeluhreinträge ** angezeigt.

## <a name="register-time"></a>Kassenzeit
### <a name="cashier-and-non-cashier-time-registrations"></a>Kassierer- und Nichtkassiererzeiterfassungen

-   Im POS:
    -   Einstempel-Vorgänge:
        -   Melden Sie sich mit einem Vorgäng ohne Kassenlade oder mit einer neuen Schicht an.
        -   Wählen Sie einen Zeituhrarbeitsgang aus.
        -   Wählen Sie einen gewünschten Vorgang aus:
            -   Einstempeln
            -   Pause für Arbeit
            -   Mittagspause
            -   Ausstempeln

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Aktueller Status:</th>
    <th>Verfügbare Vorgänge</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Einstempeln</td>
    <td><ul>
    <li>Pause für Arbeit</li>
    <li>Mittagspause</li>
    <li>Ausstempeln</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Pause für Arbeit</td>
    <td>Einstempeln</td>
    </tr>
    <tr class="odd">
    <td>Mittagspause</td>
    <td>Einstempeln</td>
    </tr>
    <tr class="even">
    <td>Ausstempeln</td>
    <td>Einstempeln</td>
    </tr>
    </tbody>
    </table>

    ![TimeClockStates ([]. /media/timeclockstates.png)]". /media/timeclockstates.png)
-   Sehen Sie die Bestätigungsmeldung an, und überprüfen Sie, ob die Uhrzeit der aktuellen Aktivität korrekt ist.
-   Arbeitsprotokoll:
    -   Klicken Sie auf **Arbeitsprotokoll**, um die Zeituhraktivität anzuzeigen.
    -   Verwenden Sei Zeitfilter, um unterschiedliche Zeitfenster auszuwählen.
    -   Wenn Sie an mehreren Filialstandorten arbeiten, Sie Ihre Zeiterfassungen von allen Shops, in denen Sie Zeit erfasst haben. Sie können den Shopfilter verwenden, um Zeiterfassungen von einem ausgewählten Shop anzuzeigen.

<!-- -->

-   Unterschiedliche Zeitzonen:
    -   Wenn Sie Zeit von einem anderen Standort (für das Kassiererarbeitsprotokoll oder mithilfe von **Zeiterfassungseinträge anzeigen** für ein Managerszenario) anzeigen und dieser Standort in einer anderen Zeitzone ist, werden die Zeiterfassungen, die Sie sehen, in Ihre lokale Zeitzone umgewandelt. Beispielsweise sind Sie ein Manager für zwei Shops, eine in Arizona und der andere im Nevada. Ein Kassierer Einstempeln erfasst ein an 9:00 Uhr in Arizona. In diesem Moment ist es in Nevada 8:00 Uhr. Wenn Sie also im Shop in Nevada sind und Zeiterfassungen anzeigen, wird die Zeiterfassung als 8 Uhr angegeben.

## <a name="view-worker-time-registrations"></a>Ansichtsarbeitskraftzeiterfassungen
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Anzeigen von Arbeitskraftzeiterfassungen und Filtern nach Shop oder Aktivitätstyp

Im POS:

-   Wählen Sie **Zeiterfassungseinträge anzeigen** aus.
-   Sie sehen Zeituhrerfassungsaktivitäten von allen Arbeitskräften, die den gleichen Filialen zugewiesen sind, denen Sie zugewiesen sind.
-   Sie können den Aktivitätstyp und Shopfilter verwenden, um Zeiterfassungen zu filtern.

## <a name="process-and-manage-time-registrations"></a>Prozess und Verwalten von Erfassungen
Dynamics 365 für Arbeitsgänge - Kleinbenutzer folgt den Workflow, um zum Berechnen, Genehmigen und Übertragen von Zeiterfassungen zur Lohnabrechnung.

### <a name="primary-operations"></a>Primäre Vorgänge

-   Berechnen
-   Genehmigen
-   An Lohnabrechnung übertragen

### <a name="other-common-operations"></a>Andere allgemeine Vorgänge

-   Massenausstempeln
-   Erfassen der Abwesenheit

Weitere Informationen zum Verarbeiten von Zeit- und Anwesenheitserfassungen finden Sie unter <https://technet.microsoft.com/en-us/library/aa573180.aspx>.


