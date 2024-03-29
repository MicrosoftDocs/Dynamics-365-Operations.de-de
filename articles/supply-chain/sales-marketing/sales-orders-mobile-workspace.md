---
title: Aufträge, mobiler Arbeitsbereich
description: Dieser Artikel enthält Informationen zum mobilen Arbeitsbereich Verkaufsaufträge Mit diesem Arbeitsbereich sind Sie jederzeit auf dem neuesten Stand hinsichtlich Ihrer Aufträge, jederzeit und überall.
author: Henrikan
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 38971f2a5f3f3d2692de0e52365e2215170101cc
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103179"
---
# <a name="sales-orders-mobile-workspace"></a>Aufträge, mobiler Arbeitsbereich

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Dieser Artikel enthält Informationen zum mobilen Arbeitsbereich **Verkaufsaufträge**. Mit diesem Arbeitsbereich sind Sie jederzeit auf dem neuesten Stand hinsichtlich Ihrer Aufträge, jederzeit und überall. 

Dieser mobile Arbeitsbereich ist für die Verwendung mit der Finanzen und Betrieb (Dynamics 365) Mobile-App vorgesehen.

## <a name="overview"></a>Übersicht
Im Arbeitsbereich mobile **Verkaufsufträge** können Sie detaillierte Informationen zu den einzelnen Aufträgen anzeigen. Diese Informationen enthalten den Auftragsstatus, Kontaktinformationen für den Debitor und die Kontaktinformationen der Auftragsannahme. Der mobile Arbeitsbereich **Aufträge** enthält eine einzige Ansicht für die Aufträge. Sie können alle Aufträge nach Debitor anzeigen, oder zeigen Sie alle Aufträge oder Informationen über einen bestimmten Auftrag an. 

Der mobile Arbeitsbereich enthält zwei Ansichten, um Ihnen dabei zu unterstützten, die detaillierten Verkaufsaufträge analysieren.

### <a name="view-all-sales-orders"></a>Alle Aufträge anzeigen
Bei dieser Ansicht werden alle Aufträge auf.

-   Wählen Sie einen der folgenden Filter aus, um den anzuzeigenden Auftrag auszuwählen:

    -   Suche von Aufträgen
    -   Nach Debitorenkonto suchen
    -   Debitorname suchen
    -   Nach Status suchen
    -   Nach Veröffentlichung suchen
    -   Nach Datum und Uhrzeit suchen
    
-   Nach der Auswahl der Aufträge können Sie die Details auf der Seite Auftrag anzeigen betrachten. Sie können die folgenden Informationen anzeigen:

    -   Debitorenname und Adressinformationen
    -   Verschiedene Daten für den Auftrag wie das angeforderte Lieferdatum und das bestätigte Versanddatum
    -   Hier können Sie Kontaktinformationen für die Auftragsannahme eingeben
    -   Kontaktinformationen für den Debitor
    -   Auftragspositionen
    -   Lieferungen, die zeigen, wie und wann ein Auftrag geliefert wurde

### <a name="view-orders-for-a-customer"></a>Aufträge für einen Kunden anzeigen
Zeigt Listen mit Aufträgen nach Debitor an.

-   Nutzen Sie einen der nachfolgenden Filter, um Aufträge für einen Debitor anzuzeigen:

    -   Suche nach Name
    -   Suche nach Konto

-   Nachdem Sie einen Debitor ausgewählt haben, können Sie Folgendes anzeigen:

    -   Debitorname und Gruppe
    -   Kontaktinformationen für den Debitor
    -   Kundenaufträge und andere Details zu Aufträgen:
    
        -   Debitorenname und Adressinformationen
        -   Verschiedene Auftragsdatumsangaben
        -   Hier können Sie Kontaktinformationen für die Auftragsannahme eingeben
        -   Kontaktinformationen für den Debitor
        -   Auftragspositionen
        -   Lieferungen, die zeigen, wie und wann ein Auftrag geliefert wurde

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen unterscheiden sich basierend auf der Version von Microsoft Dynamics 365, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Voraussetzungen, wenn Sie verwenden Supply Chain Management 
Wenn Supply Chain Management für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Aufträge** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Dynamics 365 for Operations Version 1611 mit Plattformupdate 3 oder höher verwenden
Wenn Dynamics 365 for Operations Version 1611 mit Plattformupdate 3 oder höher für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen. 

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

<td>KB 4013633 ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Verkaufsaufträge</strong> enthält. Um KB 4013633 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Den Metadatenhotfix von Microsoft Dynamics Lifecycle Services (LCS) herunterladen</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Das bereitstellbare Paket übernehmen</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Mobiler Arbeitsbereich für Aufträge</strong> veröffentlichen.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App
Laden Sie die Mobile-App für Finanzen und Vorgänge (Dynamics 365) herunter und installieren Sie sie:

-   [Für Android-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die URL Dynamics 365 ein.
3.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
4.  Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

[![Zum Aktualisieren nach unten ziehen.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Informationen zu Aufträgen für einen Debitor mithilfe dem mobilen Arbeitsbereich "Verkaufsaufträge"anzeigen

1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Auträge**.
2.  Wählen Sie **Aufträge für einen Kunden anzeigen**.
3.  Verwenden Sie Konto- oder Debitorennamen-Informationen, um den gewünschten Debitor zu suchen.
4.  Auswählen des Debitors
5.  Wählen Sie **Kontaktinformationen** oder **Aufträge** aus. Wenn Sie **Aufträge** auswählen, wird eine Liste der Aufträge für den Debitor angezeigt.
6.  **Auftrag** auswählen. Sie können nun Informationen zu Auftragspositionen, Lieferungen, Debitorenkontaktinformationen und Auftragsannahmekontaktinformationen anzeigen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

