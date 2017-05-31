---
title: "Aufträge, mobiler Arbeitsbereich"
description: "Dieses Thema enthält Informationen zum mobilen Arbeitsbereich verfügbarer Bestand, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Mit diesem Arbeitsbereich sind Sie jederzeit auf dem neuesten Stand hinsichtlich Ihrer Aufträge, jederzeit und überall."
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
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Aufträge, mobiler Arbeitsbereich

[!include[banner](../includes/banner.md)]


Dieses Thema enthält Informationen zum mobilen Arbeitsbereich verfügbarer Bestand, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Mit diesem Arbeitsbereich sind Sie jederzeit auf dem neuesten Stand hinsichtlich Ihrer Aufträge, jederzeit und überall. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Überblick über den mobilen Arbeitsbereich Aufträge
---------------------------------------------

Der mobile Arbeitsbereich **Aufträge** greift auf Microsoft Dynamics 365 for Operations zu. Sie können detaillierte Informationen zu den einzelnen Aufträgen anzeigen. Diese Informationen enthalten den Auftragsstatus, Kontaktinformationen für den Debitor und die Kontaktinformationen der Auftragsannahme. Der mobile Arbeitsbereich **Aufträge** enthält eine einzige Ansicht für die Aufträge. Sie können alle Aufträge nach Debitor anzeigen, oder zeigen Sie alle Aufträge oder Informationen über einen bestimmten Auftrag an. 

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
Bevor Sie den mobilen Arbeitsbereich **Aufträge** verwenden können, überprüfen Sie, ob Ihr Systemadministrator die folgenden Voraussetzungen bereitgestellt hat.

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
<td>Wenn Sie nicht bereits Dynamics 365 for Operations in Ihrer Organisation bereitgestellt haben, sollte Ihr Systemadministrator <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Microsoft Dynamics 365 for Operations Testumgebung bereitstellen</a> sehen.</td>
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
<td>Der mobile Arbeitsbereich <strong>Aufträge</strong> muss in der Dynamics 365 for Operations Mobile App veröffentlicht sein.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Starten Sie Dynamics 365 for Operations in Ihrem Browser.</li>
<li>Wählen Sie <strong>Mobile Arbeitsbereiche verwalten</strong> auf der <strong>Systemparameter</strong> Seite aus.</li>
<li>Wählen Sie den Arbeitsbereich <strong>Aufträge</strong> aus.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Informationen zu Aufträgen für einen Debitor mithilfe dem mobilen Arbeitsbereich anzeigen
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Auträge**.
2.  Wählen Sie **Aufträge für einen Kunden anzeigen**.
3.  Verwenden Sie Konto- oder Debitorennamen-Informationen, um den gewünschten Debitor zu suchen.
4.  Auswählen des Debitors
5.  Wählen Sie **Kontaktinformationen** oder **Aufträge** aus. Wenn Sie **Aufträge** auswählen, wird eine Liste der Aufträge für den Debitor angezeigt.
6.  **Auftrag** auswählen. Sie können nun Informationen zu Auftragspositionen, Lieferungen, Debitorenkontaktinformationen und Auftragsannahmekontaktinformationen anzeigen.





