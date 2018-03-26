---
title: "Mobiler Arbeitsbereich für Bestellungsgenehmigung"
description: "Dieses Thema enthält Informationen zum mobilen Arbeitsbereich für Bestellungsgenehmigungen, mit dem Sie Bestellungen anzeigen und auf sie durch Aktionen antworten können. Sie können beispielsweise eine Bestellung genehmigen oder ablehnen."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 24a17d3734e39815684098f694a77e96cdbc1cfe
ms.openlocfilehash: d366ae53f4a9d8e676c3bc19e0450baa254cb716
ms.contentlocale: de-de
ms.lasthandoff: 03/07/2018

---

# <a name="purchase-order-approval-mobile-workspace"></a>Mobiler Arbeitsbereich für Bestellungsgenehmigung

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Dieses Thema enthält Informationen zur **Bestellungsgenehmigung** im mobilen Arbeitsbereich. In diesem Arbeitsbereich können Sie Bestellungen anzeigen und auf sie antworten. Sie können beispielsweise eine Bestellung genehmigen oder ablehnen.
 
## <a name="overview"></a>Überblick 
Bestellungen, die Genehmigungen erfordern, durchlaufen einen Genehmigungsworkflow. Der Workflow kann unterschiedliche Schritte umfassen, die erfordern, dass mindestens eine Person eine Maßnahme ergreift. Beispielsweise kann eine Person eine Aufgabe abschließen oder die Bestellung genehmigen. 

Im Arbeitsbereich **mobile Bestellungsgenehmigung** können Sie Bestellungen vom mobilen Gerät anzeigen und beantworten. Im Arbeitsbereich können Sie die gleichen Workflowaktivitäten tätigen, die Sie im Microsoft Dynamics 365 for Finance and Operations, Enterprise Editione, Webclient tätigen können.

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen unterscheiden sich basierend auf der Version von Finance and Operations, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition verwenden 
Wenn Microsoft Dynamics 365 for Finance and Operations, Enterprise edition für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Bestellungsgenehmigung** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<td>Implementieren Sie KB 4017918.</td>
<td>Systemadministrator</td>
<td>4017918 KB ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Bestellungsgenehmigung</strong> enthält. Um KB 4017918 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laden Sie den Metadatenhotfix für Microsoft Dynamics Lifecycle Services (LCS) herunter</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Das bereitstellbare Paket übernehmen</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Mobiler Arbeitsbereich für <strong>Bestellungsgenehmigung</strong> veröffentlichen.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App
Laden Sie die mobile App für Microsoft Dynamics 365 for Unified Operations herunter und installieren Sie diese:

- [Für Androide-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
- [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden

1. Starten Sie die App auf Ihrem mobilen Gerät.
2. Geben Sie die Microsoft Dynamics 365-URL ein.
3. Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
4. Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

![Bestellungsgenehmigungsarbeitsbereich in der Liste verfügbarer Arbeitsbereiche](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Anzeigen der Ihnen zugewiesenen Aufträge
1. Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Bestellungsgenehmigung**.
2. Wählen Sie **Mir zugewiesene Aufträge**, um alle Bestellungen anzeigen, für die Sie angefordert wurden, im Bestellungsgenehmigungsworkflow aktiv zu werden.
3. Wählen Sie einen Auftrag aus. Auf der Seite **Auftragsdetails** finden Sie die Angaben im Auftragskopf und Positionen. Sie sehen auch Richtlinien für die Workflowaufgabe.
4. Wählen Sie **Buchhaltungsverteilungen**, um die Seite **Kopfbuchhaltungsverteilungen** zu öffnen.
5. Hiermit kehren Sie zur Seite **Auftragsdetails** zurück, und wählen Sie eine Position aus. Aus den Auftragspositionsdetails können Sie auch positionsspezfische Buchhaltungsverteilungen untersuchen.

## <a name="complete-an-action-on-the-purchase-order"></a>Verbinden einer Aktivität auf der Bestellung
Nachdem die Bestellung angezeigt wurde, die Ihnen zugewiesen wurde und Sie die Workflowanweisungen gelesen haben, sollten Sie bereit sein, die Ihnen zugewiesenen Aktivitäten auszuführen.

1. Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Bestellungsgenehmigung**.
2. Wählen Sie **Mir zugewiesene Aufträge**, um alle Bestellungen anzeigen, für die Sie angefordert wurden, im Bestellungsgenehmigungsworkflow aktiv zu werden.
3. Wählen Sie einen Auftrag aus, um die Details anzuzeigen.
4. Wählen Sie **Aktivitäten** aus, um die verfügbaren Aktivitäten anzuzeigen. Die Aktivitäten, die verfügbar sind, hängen von der Aufgabe ab, die Ihnen zugewiesen wurde.

    | Aufgabenaktivität    | Genehmigungsaktivität  |
    |----------------|------------------|
    | Komplett       | Genehmigen          |
    | Zurück         | Ablehnen           |
    | Änderung anfordern | Änderung anfordern   |
    | Delegat       | Delegat         |

5. Wählen Sie die entsprechende Aktivität aus.
6. Auf der Seite **Aufgabe beenden** geben Sie einen Kommentar ein. Beachten Sie, dass, wenn Sie die Aktivität **Delegieren** auswählen, müssen Sie einen Benutzer auswählen, an die Aufgabe delegiert werden soll.
7. Wählen Sie **Fertig**. Nachdem Sie den Arbeitsbereich aktualisiert haben, ist die Bestellung nicht mehr in der Liste. 

