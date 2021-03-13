---
title: Verfügbarer Lagerbestand, mobiler Arbeitsbereich
description: Dieses Thema enthält Informationen zum mobilen Arbeitsbereich für Lagerbestand. Dieser Arbeitsbereich bietet mobile Einblicke in reservierten und zur verfügbaren Bestand, jederzeit und überall.
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7d0440514369f8271004993d009ef7c3a36edb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008049"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Verfügbarer Lagerbestand, mobiler Arbeitsbereich

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zum mobilen Arbeitsbereich **Lagerbestand**. Dieser Arbeitsbereich bietet Einblicke in reservierten und verfügbaren Bestand, jederzeit und überall.

Dieser mobile Arbeitsbereich soll mit der Finance and Operations Mobile-App verwendet werden.

## <a name="overview"></a>Übersicht
Normalerweise haben Unternehmen mehrere Lieferungen und mehrere Anzeigen des Lagers jeden Tag. Diese Bewegungen ändern ständig den Status des verfügbaren Lagerbestands. Der mobile Arbeitsbereich **Lagerbestand** zeigt den Status des unternehmensübergreifenden verfügbaren Lagerbestands, damit Sie die neuesten Einblicke in die Bestandsdaten auf dem mobilen Gerät Ihrer Wahl haben. Unabhängig davon, ob Sie am Lagerort, im Einkauf, im Verkauf, in der Produktion oder in der Verwaltung arbeiten oder andere Rollen haben, können jederzeit und überall den verfügbaren Lagerbestand ansehen. 

Der mobile Arbeitsbereich gibt eine Sofortansicht des verfügbaren Bestands. Sie können den verfügbaren Lagerbestand über alle Einrichtungen, aktuelle Reservierungen und nicht reservierter, verfügbarer Lagerbestand anzeigen. Sie können auch die Artikelnummern eingeben, um verfügbaren Bestand abzufragen und eine gefilterte Suche für verfügbare Produkte oder Alternativen durchführen. 

Speziell enthält der mobile Arbeitsbereich diese Funktionen:

-   Sie können Nebenproduktnummer oder -Produktnamen suchen, um Produkte anzuzeigen, um den Status des verfügbaren Lagerbestands für angezeigt.
-   Für die ausgewählten Produkte können die folgenden Informationen angezeigt werden:

    -   Verfügbarer Lagerbestand nach Standort
    -   Verfügbaren Bestand nach Lagerort
    -   Verfügbarer Lagerbestand nach Standort
    -   Verfügbarer Lagerbestand nach Charge (für chargengesteuerte Produkte)
    -   Verfügbaren Bestand nach Bestandsstatus
    
-   Verfügbarer Lagerbestand wird folgendermaßen angezeigt:

    -   Durch physischen Bestand (Ansicht stellt den Gesamtbetrag dar).
    -   Durch physischen Reservierungen (Ansicht stellt den reservierten Betrag dar).
    -   Durch verfügbare physische Menge (Ansicht stellt den verfügbare Betrag dar, der keine Reservierungen hat).

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen unterscheiden sich basierend auf der Version von Supply Chain Management, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Voraussetzungen, wenn Sie verwenden Supply Chain Management
Wenn Supply Chain Management für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Verfügbarer Lagerbestand** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie mit Plattformupdate 3 oder höher verwenden 
Wenn das Plattformupdate 3 oder höher für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen. 

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

<td>4013633 KB ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Lagerbestand</strong> enthält. Um KB 4013633 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Den Metadatenhotfix von Microsoft Dynamics Lifecycle Services (LCS) herunterladen</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Das bereitstellbare Paket übernehmen</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Veröffentlichen Sie den mobilen Arbeitsbereich <strong>Lagerbestand</strong>.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App

Herunterladen und Installieren der Finance and Operations mobilen App:

-   [Für Android-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die URL Dynamics 365 ein.
3.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
4.  Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

    [![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Zeigt den verfügbaren Bestand für ein Produkt an, indem der mobile Arbeitsbereich für Lagerbestand verwendet wird.

1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Verfügbarer Bestand**.

2.  Wählen Sie aus **Überprüfen des verfügbaren Bestand für einen Artikel**. Sie wird eine Liste der Produkte, die sich in der Zeit-App für offline Verwendung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Wenn der Artikel nicht in der Liste ist, wählen Sie **Weitere suchen** aus. Suchen Sie Nebenproduktnummer oder wechseln Sie zu einem Suchennebenproduktnamen.

4.  Wählen Sie ein Produkt aus. Wenn der Artikel ein Bild hat das Bild, wird angezeigt.
5.  Wählen Sie eine der folgenden Optionen aus, um den Status für den verfügbaren Lagerbestand anzuzeigen:

    -   Verfügbaren Lagerbestand pro Site anzeigen
    -   Verfügbaren Lagerbestand pro Lagerort anzeigen
    -   Verfügbaren Lagerbestand pro Standort anzeigen
    -   Verfügbarer Lagerbestand nach Charge (für chargengesteuerte Produkte) anzeigen
    -   Verfügbaren Lagerbestand pro Bestandsstatus anzeigen

    Verfügbarer Lagerbestand wird folgendermaßen angezeigt:
    -   Durch physischen Bestand (Ansicht stellt den Gesamtbetrag dar).
    -   Durch physischen Reservierungen (Ansicht stellt den reservierten Betrag dar).
    -   Durch verfügbare physische Menge (Ansicht stellt den verfügbare Betrag dar, der keine Reservierungen hat).
