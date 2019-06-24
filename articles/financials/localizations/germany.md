---
title: Deutschland
description: Dieses Thema bietet eine Übersicht der Dynamics 365 for Finance and Operations-Funktionen, die für Deutschland spezifisch sind.
author: ShylaThompson
manager: AnnBe
ms.date: 04/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Germany
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 5e007e120693018e6b5b2b0f9e958b3e91844525
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558724"
---
# <a name="germany"></a>Deutschland

[!include[banner](../includes/banner.md)]

Dieses Thema enthält Informationen und Verknüpfungen zu den Ressourcen, die für juristische Personen mit einer primären Adresse in Deutschland berücksichtigt werden sollen.

## <a name="audit-file"></a>Protokolldatei
- [Deutsche Protokolldatei (GDPdU/GoBD)](emea-deu-gdpdu-audit-data-export.md)
- [Protokolldateikonfiguration anpassen](tasks/customize-german-audit-file-configuration.md)
- [Protokolldatei generieren](tasks/german-audit-file.md)
- [Protokolldateikonfiguration importieren](tasks/import-german-audit-file-configuration.md)

## <a name="depreciation"></a>Abschreibung
-   [Zusätzliche Anschaffungsabschreibung](emea-deu-additional-acquisition-depreciation.md)
-   [Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr](tasks/de-00002-depreciation.md)

## <a name="electronic-transmission-of-vat-declaration-elster"></a>Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)
- [Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)](tasks/de-00003-electronic-transmission-elster.md)
- [Elster Testmerker (PDF-Download)](https://msdnshared.blob.core.windows.net/media/2018/04/Dyn365_ElsterTestmerker.pdf)

## <a name="credit-memos-originating-from-sales"></a>Gutschriften aus Verkäufen
In diesem Artikel wird beschrieben, wie die Beschriftung definiert wird, die auf Gutschriften erscheinen, die vom Vertrieb stammen.

Auf der Seite **Juristische Personen** können Sie die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf der Registerkarte **Außenhandel und Logistik**verwenden, um die Beschriftung anzugeben, die in Gutschriften angezeigt wird, die vom Vertrieb stammen (Aufträge, Nichtartikelvertrieb und Projektvertrieb).

-   Wenn die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf **Nein** festgelegt ist, wird die Beschriftung "Gutschrift" auf alle Gutschriften gedruckt.
-   Wenn die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf **Ja** festgelegt ist, wird die Beschriftung "Rechnungskorrektur" auf Gutschriften für Aufträge, Freitextrechnungen und Projektrechnungen gedruckt.


## <a name="reports-for-germany"></a>Berichte für Deutschland

| Bericht                     |  Beschreibung  |Bericht abrufen |
|----------------------------|--------------------------|----------------------------------------|
|Deutscher Journallistenbericht|Der Bericht **Deutsche Erfassungsliste** enthält alle im Journal erfassten Buchungen, die beim Ausführen der Funktionen generiert wurden, und ist nach laufender Nummer sortiert. Dieser Bericht wird verwendet, um den Status von Hauptbuchprozessen zu überprüfen. Er wird normalerweise von leitenden Geschäftsführern, Leitern der Finanzabteilung, Leitern Compliance, Buchhaltungsleitern und Supervisors Buchhaltung und Finanzcontrollern verwendet. Weitere Informationen zu Kommissionierlistenerfassungen finden Sie unter [Deutscher Journallistenbericht](emea-deu-journal-list-report.md).|  **Hauptbuch** > **Periodisch** > **Erfassungen** > **Erstellte Erfassungen** > **Deutsches Journal**|

## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Microsoft Dynamics-Lokalisierungs-Portal: Deutschland-Bericht](https://mbs.microsoft.com/files/customer/AX/Support/supportnews/Germany.html)
- [Überblick über die elektronische Berichterstellung](../../dev-itpro/analytics/general-electronic-reporting.md)
- [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- [Lokalisierung und rechtliche Funktionen](../../dev-itpro/lcs-solutions/country-region.md?toc=/fin-and-ops/toc.json)
- [Erstellen Sie eine Umsatzsteuervoranmeldung im XML-Format, ohne Daten für ELSTER (Whitepaper)](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/VATdeclarationXMLELSTER)
