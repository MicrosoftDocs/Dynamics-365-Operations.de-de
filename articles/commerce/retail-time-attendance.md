---
title: Zeit- und Anwesenheitsverwaltung in Retail
description: Dieses Thema beschreibt Szenarien, die für die Verwaltung von Zeit und Anwesenheit in Dynamics 365 Commerce unterstützt werden.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022676"
---
# <a name="time-and-attendance-management-in-retail"></a>Zeit- und Anwesenheitsverwaltung in Retail

[!include [banner](includes/banner.md)]

Dieses Thema beschreibt Szenarien, die für die Verwaltung von Zeit und Anwesenheit in Dynamics 365 Commerce unterstützt werden.

## <a name="manage-worker-setup-and-scheduling"></a>Verwalten Sie Arbeitskrafteinstellung und Feinterminierung

### <a name="initial-configuration"></a>Ausgangskonfiguration

- Führen Sie den Konfigurationsassistenten aus.
- Registrieren Sie Arbeitskräfte als Zeiterfassungsarbeitskräfte.

### <a name="plan-worker-schedules"></a>Planen von Arbeitskraftzeitplänen

- Wenden Sie Profile durch Verwendung der Arbeitsplanung an. Weitere Informationen zu [Arbeitszeitprofilen finden Sie unter](https://technet.microsoft.com/library/aa551234.aspx)

Informationen über die Konfigurationsschritte, finden [Zeit und Anwesenheit](https://technet.microsoft.com/library/aa496971.aspx) Sie unter.

### <a name="commerce-specific-configuration"></a>Commerce-spezifische Konfiguration

- Aktivieren Sie ein Funktionsprofil für die Zeiterfassung für Arbeitskräfte, für die Sie Zeiterfassungen aktivieren möchten. Klicken Sie auf **POS-Funktionensprofile** &gt; **Funktionen** &gt; **POS-Zeiterfassungen** &gt; **Zeiterfassungen aktivieren.**
- Konfigurieren Sie Point-of-Sale-Berechtigungsgruppen (POS), um die Berechtigung zum Anzeigen von Zeiterfassungseinträgen zu aktivieren. Diese Berechtigung ermöglicht einem Benutzer die Anzeige der Zeiterfassungen anderer Arbeitskräfte im Shop (und von jedem anderen Shops, dem der Benutzer zugeordnet ist, über das Adressbuch). Sie sollten diese Berechtigung für eine Managerrolle aber nicht für eine Kassiererrolle aktivieren. Klicken Sie auf **POS-Berechtigungsgruppen** &gt; **Zeiterfassungseinträge anzeigen.**

## <a name="register-time"></a>Kassenzeit

### <a name="cashier-and-non-cashier-time-registrations"></a>Kassierer- und Nichtkassiererzeiterfassungen

- Im POS:

    - Einstempel-Vorgänge:

        - Melden Sie sich mit einem Vorgäng ohne Kassenlade oder mit einer neuen Schicht an.
        - Wählen Sie einen Zeituhrarbeitsgang aus.
        - Wählen Sie einen gewünschten Vorgang aus:

            - Einstempeln
            - Pause für Arbeit
            - Mittagspause
            - Ausstempeln

        <table>
        <thead>
        <tr>
        <th>Aktueller Status:</th>
        <th>Verfügbare Vorgänge</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Einstempeln</td>
        <td>
        <ul>
        <li>Pause für Arbeit</li>
        <li>Mittagspause</li>
        <li>Ausstempeln</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Pause für Arbeit</td>
        <td>Einstempeln</td>
        </tr>
        <tr>
        <td>Mittagspause</td>
        <td>Einstempeln</td>
        </tr>
        <tr>
        <td>Ausstempeln</td>
        <td>Einstempeln</td>
        </tr>
        </tbody>
        </table>

        [![Status der Zeituhr](./media/timeclockstates.png)](./media/timeclockstates.png)

- Sehen Sie die Bestätigungsmeldung an, und überprüfen Sie, ob die Uhrzeit der aktuellen Aktivität korrekt ist.
- Arbeitsprotokoll:

    - Klicken Sie auf **Arbeitsprotokoll**, um die Zeituhraktivität anzuzeigen.
    - Verwenden Sei Zeitfilter, um unterschiedliche Zeitfenster auszuwählen.
    - Wenn Sie an mehreren Filialstandorten arbeiten, Sie Ihre Zeiterfassungen von allen Shops, in denen Sie Zeit erfasst haben. Sie können den Shopfilter verwenden, um Zeiterfassungen von einem ausgewählten Shop anzuzeigen.

- Unterschiedliche Zeitzonen:

    - Wenn Sie Zeit von einem anderen Standort (für das Kassiererarbeitsprotokoll oder mithilfe von **Zeiterfassungseinträge anzeigen** für ein Managerszenario) anzeigen und dieser Standort in einer anderen Zeitzone ist, werden die Zeiterfassungen, die Sie sehen, in Ihre lokale Zeitzone umgewandelt. Beispielsweise sind Sie ein Manager für zwei Shops, eine in Arizona und der andere im Nevada. Ein Kassierer Einstempeln erfasst ein an 9:00 Uhr in Arizona. In diesem Moment ist es in Nevada 8:00 Uhr. Wenn Sie also im Shop in Nevada sind und Zeiterfassungen anzeigen, wird die Zeiterfassung als 8 Uhr angegeben.

## <a name="view-worker-time-registrations"></a>Zeiterfassungsarbeitskräfte anzeigen

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Anzeigen von Arbeitskraftzeiterfassungen und Filtern nach Shop oder Aktivitätstyp

Im POS:

- Wählen Sie **Zeiterfassungseinträge anzeigen** aus.
- Sie sehen Zeituhrerfassungsaktivitäten von allen Arbeitskräften, die den gleichen Filialen zugewiesen sind, denen Sie zugewiesen sind.
- Sie können den Aktivitätstyp und Shopfilter verwenden, um Zeiterfassungen zu filtern.

## <a name="process-and-manage-time-registrations"></a>Verarbeiten und Verwalten von Zeit- und Anwesenheitserfassungen

Ein Commerce-Benutzer folgt dem Workflow, um Zeiterfassungen zu berechnen, zu genehmigen und in die Lohnabrechnung zu übertragen.

### <a name="primary-operations"></a>Primäre Vorgänge

- Berechnen
- Genehmigen
- An Lohnabrechnung übertragen

### <a name="other-common-operations"></a>Andere allgemeine Vorgänge

- Massenausstempeln
- Erfassen der Abwesenheit

Weitere Informationen dazu, wie Anwesenheitserfassungen in den Erfassungen verarbeitet werden, finden [Anwesenheitserfassungen und Prozesszeit](https://technet.microsoft.com/library/aa573180.aspx).
