---
title: "Erfassungseinträge und Transaktionen anzeigen"
description: "Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8607f27bc36d62865b03f433c24c90763e8e0bec
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="view-journal-entries-and-transactions"></a>Erfassungseinträge und Transaktionen anzeigen

[!include[banner](../includes/banner.md)]


Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen. 

Benutzer, die Erfassungen und Transaktionen anzeigen möchten, haben mehrere Möglichkeiten für den Datenzugriff. Sie können Anfragenseiten nutzen, die eine Detallanzeige ermöglichen, oder sie können verschiedene Berichtsoptionen im Hauptbuch verwenden.

## <a name="voucher-transactions"></a>Belegtransaktionen
**Belegtransaktionen** ist eine Anfragenseite, in der Sie aus verschiedenen Tabellen und Feldern auswählen können, um Kriterien für den Saldo oder die Transaktion anzugeben, die Sie suchen. So können Sie z. B. alle Transaktionen für ein bestimmtes Datum oder ein Konto oder alle Transaktionen des Typs **Benutzung** anzeigen, die sich auf einer bestimmten Buchungsebene befinden. Standardmäßig zeigt die Seite die Erfassungsnummer, Beleg, Datum und Hauptkonto an, Sie können jedoch zusätzliche Tabellen, Felder und Kriterien hinzufügen, um die Suche einzugrenzen.

## <a name="audit-trail"></a>Audit-Trail
**Audit-Trail** ist eine Anfragenseite, die Transaktionsarten, Beschreibungen, Transaktionsersteller und -datum anzeigt. Von der **Audit-Trail**-Anfragenseite können Sie die Belegtransaktionen anzeigen.

## <a name="financial-reports"></a>Finanzberichte
Sie können Hauptbuchtransaktionen auch untersuchen und analysieren, indem Sie Finanzberichte ausführen. Da das Design von Finanzberichten auf Konten, Dimensionen, Kontokategorien oder einer Kombination dieser drei basieren kann, können Sie die Transaktionen anzeigen, indem Sie auf verschiedene Weise Details anzeigen. Wenn Sie weitere Informationen zu Hauptbuchtransaktionen erfordern, können Sie auch mehrere Transaktionseigenschaften als Teil des Berichtsdesigns einschließen. Wenn Sie darüber hinaus die Transaktionen anzeigen möchten, aus denen sich ein Hauptbuchsaldo zusammensetzt, können Sie Details für die Kontotransaktionen anzeigen,genau wie aus der **Zwischenbilanz**-Listenseite.

## <a name="ledger-reports"></a>Sachkonto – Berichte
Neben den Finanzberichten können Sie die folgenden Sachkontoberichte verwenden, um Hauptbuchtransaktionen anzuzeigen:

-   **Dimensionsaufstellung** - Dieser Bericht zeigt Buchungen nach Tag und Konto und es gibt auch Optionen, um Transaktionen nach Dimension und Periode anzuzeigen.
-   **Sachkontobuchungsliste** – Dieser Bericht zeigt Transaktionen in Transaktions-, Buchhaltungs- und Berichtswährungen für ein Konto an.
-   **Erfassung drucken** – Dieser Bericht zeigt das Ergebnis einer gebuchte Erfassung an. Sie können den Bericht auf Basis der Nummer der Stapelverarbeitungserfassung oder des Erfassungstyp ausführen oder zusätzliche Felder hinzufügen.
-   **Gebuchte Posten nach Erfassung** – In diesem Bericht werden die Transaktionen, die in einer Erfassung gebucht wurden gruppiert nach Beleg angezeigt.
-   **Sachkontopostenliste nach Datum** – Dieser Bericht zeigt alle Transaktionen nach Datum, zusammen mit der Erfassungsnummer, dem Beleg und dem Sachkonto an. Darin werden auch die Transaktionen in den Transaktions-, Buchhaltungs- und Berichtswährungen angezeigt.
-   **Buchungsgrundlage** – Dieser Transaktionsbericht zeigt das Konto nach Efassuung und nach Transaktions-, Buchhaltungs- und Berichtswährung an. Es wird auch jede Position der Erfassung angezeigt, die als Ausgleich verwendet wurde.


##<a name="see-also"></a>Siehe auch
- [Kontosalden für das Hauptbuch](general-ledger-account-balances.md) 
- [Buchhaltungsquellen-Explorer](..\accounts-payable\accounting-source-explorer.md)
- [Finanzberichterstellung](financial-reporting-getting-started.md)




