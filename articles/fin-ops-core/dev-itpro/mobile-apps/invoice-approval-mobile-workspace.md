---
title: Rechnungsgenehmigungen im mobilen Arbeitsbereich
description: Dieses Thema enthält Informationen zur Rechnungsgenehmigung im mobilen Arbeitsbereich.
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c3414d6ef5f2df62f37f1ef2e7e2ff43ce040e5e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752249"
---
# <a name="invoice-approvals-mobile-workspace"></a>Rechnungsgenehmigungen im mobilen Arbeitsbereich

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur **Rechnungsgenehmigung** im mobilen Arbeitsbereich. Der Arbeitsbereich enthält eine Liste von Rechnungen, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurden. 

Dieser mobile Arbeitsbereich soll mit der Finance and Operations Mobile-App verwendet werden.

## <a name="overview"></a>Übersicht

Mit dem mobilen Arbeitsbereich **Rechnungsgenehmigungen** können Mitarbeiter und Vorgesetzte für Kreditorenkonten Rechnungen anzeigen, die ihnen als Teil des Kreditorenrechnungskopfworkflowprozesses zugewiesen wurden. Sie können Rechnungsinformationen und sogar die Positions- und Verteilungsdetails anzeigen, um informierte Genehmigungsentscheidungen zu treffen. Über den Arbeitsbereich können Sie Maßnahmen ergreifen, um die Rechnung durch den Workflowprozess durchlaufen zu lassen. 

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie diesen mobilen Arbeitsbereich verwenden können, müssen die folgenden Voraussetzungen erfüllt werden.

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
<td>Microsoft Dynamics 365 Finance muss in der Organisation bereitgestellt werden.</td>
<td>Systemadministrator</td>
<td>Siehe auch <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a>
</td>
</tr>
<tr class="even">
<td>Der mobile Arbeitsbereich <strong>Rechnungsgenehmigungen</strong> muss bereitgestellt werden.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App

Herunterladen und Installieren der Finance and Operations mobilen App:

-   [Für Android-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die Microsoft Dynamics 365-URL ein.
3.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
4.  Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

    [![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Genehmigen von Rechnungen mit dem mobilen Arbeitsbereich für Rechnungsgenehmigungen
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Rechnungsgenehmigungen**.
2.  Wählen Sie die Rechnung aus, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurde.
3.  Auf der Seite **Rechnungsdetails** können Sie die Rechnungskopfinformationen prüfen, beispielsweise Kreditor- und die Datumsinformationen.
4.  Wählen Sie eine Position in der Rechnung aus, um ausführlichere Informationen dazu in der Ansicht **Rechnungspositionsdetails** anzuzeigen.
5.  Wählen Sie in der Ansicht **Rechnungspositionsdetails** **Verteilungen** aus, um Positionsverteilungen anzuzeigen. Hier können Sie die Buchhaltung für die Rechnungsposition anzeigen. Die Informationen, die angezeigt werden, schließen die Finanzdimensionen und das Hauptkonto ein.
6.  Wählen Sie auf der Seite **Rechnungsdetails** **Verteilungen** aus, um alle Verteilungen anzuzeigen. Hier können Sie die Buchhaltung für die gesamte Rechnung anzeigen. Die Informationen, die angezeigt werden, schließen die Finanzdimensionen und das Hauptkonto ein. 
7.  Wählen Sie die Ansicht **Anhänge** aus, um alle Hinweise oder Dateien anzuzeigen, die der Rechnung zugeordnet sind.
8.  Wählen Sie auf der Seite **Rechnungsdetails** eine geeignete Workflowaktivität aus, um den Prüfprozess abzuschließen.
9.  Wählen Sie **Fertig**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]