---
title: Erfassungseinträge und Transaktionen anzeigen
description: Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen.
author: aprilolson
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71491e3fbe09314ec41652fa41c2e037520ee332
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715228"
---
# <a name="view-journal-entries-and-transactions"></a>Erfassungseinträge und Transaktionen anzeigen

[!include [banner](../includes/banner.md)]

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


## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Kontosalden für Sachkonto](general-ledger-account-balances.md) 
- [Buchhaltungsquellen-Explorer](../accounts-payable/accounting-source-explorer.md)
- [Finanzberichterstellung – Übersicht](financial-reporting-getting-started.md)
- [Journaleinträge oder Buchungen anzeigen](tasks/view-journal-entries-or-transactions.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
