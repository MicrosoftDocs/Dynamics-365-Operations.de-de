---
title: Informationen zu Deutschland
description: Dieser Artikel bietet eine Übersicht der Dynamics 365 Finance-Funktionen, die für Deutschland spezifisch sind.
author: AdamTrukawka
ms.date: 05/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: atrukawk
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 06d89cbf9df853d6e243678897b08b744e801d6c
ms.sourcegitcommit: 6c05bcd27e6ee72f01cb66e2cfd1e929e0365830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/16/2022
ms.locfileid: "9854064"
---
# <a name="germany-overview"></a>Informationen zu Deutschland

[!include[banner](../includes/banner.md)]

Dieser Artikel enthält Informationen und Verknüpfungen zu den Ressourcen, die für juristische Personen mit einer primären Adresse in Deutschland berücksichtigt werden sollen.

## <a name="audit-file"></a>Protokolldatei
- [Deutsche Protokolldatei (GDPdU/GoBD) – Übersicht](emea-deu-gdpdu-audit-data-export.md)
- [Anpassen der deutschen Protokolldateikonfiguration](tasks/customize-german-audit-file-configuration.md)
- [Generieren Sie deutsche Protokolldatei](tasks/german-audit-file.md)
- [Deutsche Protokolldateikonfiguration importieren](tasks/import-german-audit-file-configuration.md)

## <a name="depreciation"></a>Abschreibung
-   [Zusätzliche Anschaffungsabschreibung](emea-deu-additional-acquisition-depreciation.md)
-   [Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr](tasks/de-00002-depreciation.md)

## <a name="vat-declaration"></a>MwSt.-Erklärung 
-   [Umsatzsteuererklärung für Deutschland](emea-deu-vat-declaration-germany.md)

## <a name="electronic-transmission-of-vat-declaration-elster"></a>Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)
Diese Funktion ist veraltet. Weitere Informationen finden Sie unter [Entfernte und außer Betrieb genommene Funktionen](../get-started/removed-deprecated-features-finance.md#elster-declaration-for-germany-design-based-on-reporting-codes-electronic-tax-declaration-log-menu-item-and-page-electronic-tax-declaration-setup-menu-item-and-page-german-report-layout-taxreport_de-ssrs-format). Weitere Informationen zur Mehrwertsteuererklärung finden Sie unter [Mehrwertsteuererklärung (Deutschland)](emea-deu-vat-declaration-germany.md)
- [Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)](tasks/de-00003-electronic-transmission-elster.md)
- [ELSTER-Steuererklärung für Deutschland](emea-de-vat-declaration.md)

## <a name="electronic-invoices-in-germany"></a>Elektronische Rechnungen in Deutschland
- [Elektronische Rechnungen für Kunden exportieren](emea-deu-e-invoices.md)

## <a name="credit-memos-originating-from-sales"></a>Gutschriften aus Verkäufen
In diesem Artikel wird beschrieben, wie die Beschriftung definiert wird, die auf Gutschriften erscheinen, die vom Vertrieb stammen.

Auf der Seite **Juristische Personen** können Sie die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf der Registerkarte **Außenhandel und Logistik** verwenden, um die Beschriftung anzugeben, die in Gutschriften angezeigt wird, die vom Vertrieb stammen (Aufträge, Nichtartikelvertrieb und Projektvertrieb).

-   Wenn die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf **Nein** festgelegt ist, wird die Beschriftung "Gutschrift" auf alle Gutschriften gedruckt.
-   Wenn die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf **Ja** festgelegt ist, wird die Beschriftung "Rechnungskorrektur" auf Gutschriften für Aufträge, Freitextrechnungen und Projektrechnungen gedruckt.


## <a name="reports-for-germany"></a>Berichte für Deutschland
[Deutscher Journallistenbericht](emea-deu-journal-list-report.md)

## <a name="intra-community-reporting"></a>Intra-Community-Berichterstattung
-   [EU-Verkaufsliste für Deutschland](emea-deu-eu-sales-list.md)
-   [Intrastat](emea-deu-intrastat.md)

## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Microsoft Dynamics-Lokalisierungs-Portal: Deutschland-Bericht](https://mbs.microsoft.com/files/customer/AX/Support/supportnews/Germany.html)
- [Überblick über die elektronische Berichterstellung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
- [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- [Lokalisierung und rechtliche Funktionen](../../fin-ops-core/dev-itpro/lcs-solutions/country-region.md?toc=%2ffin-and-ops%2ftoc.json)
- [Erstellen Sie eine Umsatzsteuervoranmeldung im XML-Format, ohne Daten für ELSTER (Whitepaper)](https://www.microsoft.com/download/details.aspx?id=101929)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
