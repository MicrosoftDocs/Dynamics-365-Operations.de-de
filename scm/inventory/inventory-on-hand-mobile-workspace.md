---
title: "Verfügbarer Lagerbestand, mobiler Arbeitsbereich"
description: "Dieses Thema enthält Informationen zum mobilen Arbeitsbereich verfügbarer Bestand, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Dieser Arbeitsbereich bietet mobile Einblicke in reservierten und zur verfügbaren Bestand, jederzeit und überall."
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
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Verfügbarer Lagerbestand, mobiler Arbeitsbereich

[!include[banner](../includes/banner.md)]


Dieses Thema enthält Informationen zum mobilen Arbeitsbereich verfügbarer Bestand, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Dieser Arbeitsbereich bietet mobile Einblicke in reservierten und zur verfügbaren Bestand, jederzeit und überall.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Übersicht über den verfügbaren Lagerbestand, mobiler Arbeitsbereich
--------------------------------------------------

Normalerweise haben Unternehmen mehrere Lieferungen und mehrere Anzeigen des Lagers jeden Tag. Diese Bewegungen ändern ständig den Status des verfügbaren Lagerbestands. Der mobile Arbeitsbereich **Verfügbarer Bestand** zeigt den Status des unternehmensübergreifenden verfügbaren Lagerbestands, damit Sie die neuesten Einblicke in die Bestandsdaten auf dem mobilen Gerät Ihrer Wahl haben. Unabhängig davon, ob Sie am Lagerort, im Einkauf, im Verkauf, in der Produktion oder in der Verwaltung arbeiten oder andere Rollen haben, können jederzeit und überall den verfügbaren Lagerbestand ansehen. 

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
Bevor Sie den mobilen Arbeitsbereich **Verfügbarer Lagerbestand** verwenden können, überprüfen Sie, ob Ihr Systemadministrator die folgenden Voraussetzungen bereitgestellt hat.

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
<td>Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder späterem muss implementiert werden.</td>
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
<td>Der mobile Arbeitsbereich <strong>Verfügbarer Lagerbestand</strong> muss in der Dynamics 365 for Operations Mobile App veröffentlicht sein.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Starten Sie Dynamics 365 for Operations in Ihrem Browser.</li>
<li>Wählen Sie <strong>Mobile Arbeitsbereiche verwalten</strong> auf der <strong>Systemparameter</strong> Seite aus.</li>
<li>Wählen Sie den Arbeitsbereich <strong>Verfügbarer Lagerbestand</strong>.</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Zeigt den verfügbaren Bestand für ein Produkt an, indem den Sie den mobilen Arbeitsbereich für Verfügbaren Bestand verwenden
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Verfügbarer Bestand**.
2.  Wählen Sie aus **Überprüfen des verfügbaren Bestand für einen Artikel**. Sie wird eine Liste der Produkte, die sich in der Zeit-App für offline Verwendung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sollten Entwickler sehen [Dynamics 365 for Operations mobile Plattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
3.  Wenn der Artikel nicht in der Liste, wählen Sie **Weitere suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suchen Sie Nebenproduktnummer oder wechseln Sie zu einem Suchennebenproduktnamen.
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






