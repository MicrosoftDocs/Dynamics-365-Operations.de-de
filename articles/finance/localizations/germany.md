---
title: Deutschland – Übersicht
description: Dieses Thema bietet eine Übersicht der Dynamics 365 Finance-Funktionen, die für Deutschland spezifisch sind.
author: ShylaThompson
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1148084f2b4d822615c00a3244c5963fe74aa9fc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890312"
---
# <a name="germany-overview"></a>Deutschland – Übersicht

[!include[banner](../includes/banner.md)]

Dieses Thema enthält Informationen und Verknüpfungen zu den Ressourcen, die für juristische Personen mit einer primären Adresse in Deutschland berücksichtigt werden sollen.

## <a name="audit-file"></a>Protokolldatei
- [Deutsche Protokolldatei (GDPdU/GoBD) – Übersicht](emea-deu-gdpdu-audit-data-export.md)
- [Anpassen der deutschen Protokolldateikonfiguration](tasks/customize-german-audit-file-configuration.md)
- [Generieren Sie deutsche Protokolldatei](tasks/german-audit-file.md)
- [Deutsche Protokolldateikonfiguration importieren](tasks/import-german-audit-file-configuration.md)

## <a name="depreciation"></a>Abschreibung
-   [Zusätzliche Anschaffungsabschreibung](emea-deu-additional-acquisition-depreciation.md)
-   [Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr](tasks/de-00002-depreciation.md)

## <a name="electronic-transmission-of-vat-declaration-elster"></a>Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)
- [Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)](tasks/de-00003-electronic-transmission-elster.md)
- [Elster Testmerker (PDF-Download)](https://msdnshared.blob.core.windows.net/media/2018/04/Dyn365_ElsterTestmerker.pdf)
- [Umsatzsteuererklärung für Deutschland](emea-de-vat-declaration.md)

## <a name="electronic-invoices-in-germany"></a>Elektronische Rechnungen in Deutschland
- [Elektronische Rechnungen für Kunden exportieren](emea-deu-e-invoices.md)

## <a name="credit-memos-originating-from-sales"></a>Gutschriften aus Verkäufen
In diesem Artikel wird beschrieben, wie die Beschriftung definiert wird, die auf Gutschriften erscheinen, die vom Vertrieb stammen.

Auf der Seite **Juristische Personen** können Sie die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf der Registerkarte **Außenhandel und Logistik** verwenden, um die Beschriftung anzugeben, die in Gutschriften angezeigt wird, die vom Vertrieb stammen (Aufträge, Nichtartikelvertrieb und Projektvertrieb).

-   Wenn die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf **Nein** festgelegt ist, wird die Beschriftung "Gutschrift" auf alle Gutschriften gedruckt.
-   Wenn die Option **Rechnungskorrektur auf Verkaufsgutschrift drucken** auf **Ja** festgelegt ist, wird die Beschriftung "Rechnungskorrektur" auf Gutschriften für Aufträge, Freitextrechnungen und Projektrechnungen gedruckt.


## <a name="reports-for-germany"></a>Berichte für Deutschland

| Bericht                     |  Beschreibung  |Bericht abrufen |
|----------------------------|--------------------------|----------------------------------------|
|Deutscher Journallistenbericht|Der Bericht **Deutsche Erfassungsliste** enthält alle im Journal erfassten Buchungen, die beim Ausführen der Funktionen generiert wurden, und ist nach laufender Nummer sortiert. Dieser Bericht wird verwendet, um den Status von Hauptbuchprozessen zu überprüfen. Er wird normalerweise von leitenden Geschäftsführern, Leitern der Finanzabteilung, Leitern Compliance, Buchhaltungsleitern und Supervisors Buchhaltung und Finanzcontrollern verwendet. Weitere Informationen zu Kommissionierlistenerfassungen finden Sie unter [Deutscher Journallistenbericht](emea-deu-journal-list-report.md).|  **Hauptbuch** > **Periodisch** > **Erfassungen** > **Erstellte Erfassungen** > **Deutsches Journal**|

## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Microsoft Dynamics-Lokalisierungs-Portal: Deutschland-Bericht](https://mbs.microsoft.com/files/customer/AX/Support/supportnews/Germany.html)
- [Überblick über die elektronische Berichterstellung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
- [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- [Lokalisierung und rechtliche Funktionen](../../fin-ops-core/dev-itpro/lcs-solutions/country-region.md?toc=%2ffin-and-ops%2ftoc.json)
- [Erstellen Sie eine Umsatzsteuervoranmeldung im XML-Format, ohne Daten für ELSTER (Whitepaper)](https://www.microsoft.com/download/details.aspx?id=101929)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]