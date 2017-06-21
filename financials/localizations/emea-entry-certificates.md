---
title: "EU-Gelangensbestätigung"
description: "Dieser Artikel enthält Informationen zu Gelangensbestätigungen der Europäischen Union (EU)."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 415e8ec91f3968883cb4e7ece10d8a26782bac1b
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="eu-entry-certificates"></a>EU-Gelangensbestätigungen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu Gelangensbestätigungen der Europäischen Union (EU).

Sie können die folgenden Aufgaben für eine EU-Gelangensbestätigung ausführen:

-   Erstellen und geben Sie eine EU-Gelangensbestätigung mit einem Lieferschein oder der Debitorenrechnung für die Lieferung von Artikeln oder Dienstleistungen an EU-Länder/-Regionen aus.
-   Empfangen Sie die EU-Gelangensbestätigung, die von einem EU-Debitor unterzeichnet wurde.
-   Laden Sie die unterzeichnete EU-Gelangensbestätigung hoch, die vom Debitor oder von einem Dritten, der für die Lieferung von Artikeln an den Debitor zuständig ist, entgegengenommen wurde.
-   Ordnen Sie die hochgeladene EU-Gelangensbestätigung einer Debitorenrechnung zu.
-   Aktualisieren Sie den Status der hochgeladenen EU-Gelangensbestätigung.

## <a name="prerequisites"></a>Erforderliche Komponenten
In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Voraussetzung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Land/Region</td>
<td>Die primäre Adresse der juristischen Person muss in einem EU-Mitgliedsstaat sein.</td>
</tr>
<tr class="even">
<td>Zugehörige Einrichtungsaufgaben</td>
<td><ul>
<li>Wählen Sie <strong>Verwaltung der Gelangensbestätigung aktivieren</strong> und <strong>Ausstellung der Gelangensbestätigung aktivieren</strong> auf der <strong>Debitorenparameter</strong>-Seite aus.</li>
<li>Auf der <strong>Debitoren</strong>-Seite auf dem <strong>Rechnung und Lieferung</strong>-Inforegister, wählen Sie die <strong>Gelangensbestätigung erforderlich</strong>-Option aus, um anzugeben, dass eine EU-Gelangensbestätigung für den Debitor obligatorisch ist. Aktivieren Sie die Option <strong>Gelangensbestätigung ausstellen</strong>, um eine EU-Gelangensbestätigung der juristischen Person für den Debitor auszustellen.</li>
<li>Wählen Sie auf der <strong>Debitorenparameter</strong>-Seite einen Nummernkreiscode für die <strong>Gelangensbestätigung</strong>-Referenz aus.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zugehörige Transaktionen</td>
<td><ul>
<li>Erstellen eines Debitorenkontos.</li>
<li>Erstellen Sie einen Auftrag.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>Erstellen, Erfassen und Hochladen einer EU-Gelangensbestätigung
Sie können eine EU-Gelangensbestätigung automatisch oder manuell erstellen. Eine EU-Eingangssbestätigung wird automatisch erstellt und gedruckt, wenn Sie einen Lieferschein oder eine Rechnung für einen Debitor über die Seite **Lieferschein buchen** oder **Rechnung buchen**. Um eine EU-Eingangsbestätigung für eine Kundenrechnung manuell zu erstellen oder neu zu drucken, verwenden Sie die Seite**Rechnungserfassung**-. Darüber hinaus können Sie mithilfe der Seite **Gelangensbestätigungsjournal** Details zu einer EU-Gelangensbestätigung eingeben, die von einem Dritten ausgestellt wurde.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>Eine EU-Gelangensbestätigung automatisch oder manuell erstellen

Sie können eine EU-Gelangensbestätigung automatisch erstellen, indem Sie einen Lieferschein auf der Seite **Alle Aufträge** verwenden, oder indem Sie eine Rechnung auf der Seite **Auftrag** verwenden. Um eine EU-Gelangensbestätigung manuell zu erstellen, können Sie eine Rechnung auf der Seite **Rechnungserfassung** verwenden. Sie müssen den Status einer Gelangensbestätigung der Rechnung ändern, bevor Sie eine EU-Gelangensbestätigung manuell erstellen.

### <a name="registering-an-eu-entry-certificate"></a>Erfassen einer EU-Gelangensbestätigung

Wenn eine Erfassung erforderlich ist, können Sie mithilfe der Seite **Gelangensbestätigungsjournal** Details zu einer EU-Gelangensbestätigung erfassen, die von einem Dritten ausgestellt wurde.

### <a name="uploading-a-received-eu-entry-certificate"></a>Hochladen einer empfangenen EU-Gelangensbestätigung

Verwenden Sie die Seite **Anhänge**, um eine empfangene EU-Gelangensbestätigung hochzuladen, die von einem EU-Debitor unterzeichnet wurde. Nachdem die Bescheinigung hochgeladen wurde, können Sie sie als Nachweis der Lieferung der Artikel einer Rechnung zuordnen. Dieser Nachweis ist erforderlich wenn Sie eine Rechnung ausstellen müssen, die keine Mehrwertsteuer (VAT) umfasst. Sie wird außerdem während der Überwachung verwendet.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Optional: Aktualisieren des Status der Gelangensbestätigung und Drucken des Status einer Rechnung

Sie können den Status der Gelangensbestätigung und den Druckstatus einer Debitorenrechnung aktualisieren, indem Sie die Seite **Rechnungserfassung** verwenden.

## <a name="technical-information-for-system-administrators"></a>Technische Informationen für Systemadministratoren
Wenn Sie keinen Zugriff auf die Seiten für die Durchführung dieser Aufgabe haben, wenden Sie sich mit den Informationen aus der folgenden Tabelle an Ihren Systemadministrator.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Voraussetzung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sicherheitsrollen und Aufgaben</td>
<td>Um eine EU-Gelangensbestätigung für Artikel oder Dienstleistungen einzurichten und zu erstellen, müssen Sie Mitglied einer Sicherheitsrolle sein, die die folgenden Aufgaben umfasst:
<ul>
<li><strong>Sachbearbeiter Debitoren</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Kundendienstmitarbeiter</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Verkaufssachbearbeiter</strong> (TradeSalesClerk)</li>
<li><strong>Sachbearbeiter Versand</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>






