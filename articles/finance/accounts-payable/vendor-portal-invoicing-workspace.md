---
title: Arbeitsbereich für Kreditor-Kooperationsrechungen
description: In diesem Thema wird erläutert, wie Sie Kreditorenrechnungen anzeigen und Rechnungen vom Arbeitsberiech"Kreditorenzusammenarbeit-Rechnungsstellung" senden können.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3f4729a8a788f4f5b2b2e9923f515b86590b946
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188807"
---
# <a name="vendor-collaboration-invoicing-workspace"></a>Arbeitsbereich für Kreditor-Kooperationsrechungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Kreditorenrechnungen anzeigen und Rechnungen vom Arbeitsberiech"Kreditorenzusammenarbeit-Rechnungsstellung" senden können.

Der Arbeitsbereich **Kreditor-Kooperationsrechnung** kann verwendet werden, um Kreditorenrechnungsinformationen anzuzeigen und Rechnungen an das System mithilfe der Workflowfunktion zu senden.


## <a name="vendor-collaboration-invoicing-workspace"></a>Arbeitsbereich für Kreditorkooperationsrechnungen

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die Kacheln **Zusammenfassung** bieten einen Überblick über die Rechnungen für den ausgewählten Kreditor. Sie können Rechnungen nach Status anzeigen.
-   Entwurfsrechnungen wurden nicht an den Workflow übermittelt.
-   Gesendete, nicht genehmigte Rechnungen sind jene Rechnungen, die vom Lieferanten übermittelt wurden, aber noch nicht in der Anwendung gebucht sind.
-   Genehmigte, nicht bezahlte Rechnungen sind jene Rechnungen, die gebucht aber noch nicht vollständig bezahlt sind.
-   Bezahlte Rechnungen sind jene, die in der Anwendung vollständig bezahlt wurden.

Durch Klicken auf eine Kachel öffnet sich eine gefilterte Ansicht der Seite **Rechnungsliste**.

### <a name="tabular-lists"></a>Tabellarische Listen

Im Abschnitt **Tabellarische Listen** wird der Status der Rechnungsstellung auf ähnliche Weise aufgeteilt, wie die Zusammenfassung der Kacheln: Entwurfs- und übermittelte nicht genehmigte Listen. Im Entwurfstatus kann eine Rechnung an einen Workflow gesendet oder gelöscht werden. Die letzte tabellarische Liste ist eine Möglichkeit, Rechnungen zu suchen. Sie können Ihre Suche filtern, um schnellere Suchen zuzulassen.

### <a name="all-vendor-invoices-list-page"></a>Listenseite "Alle Kreditorenrechnungen"

Sie können alle gebuchten und nicht gebuchten Kreditorenrechnungen auf der Listenseite **Kreditor-Kooperationsrechnungen** anzeigen. Sie können mit dieser Listenseite den Zahlungsstatus der Rechnungen anzuzeigen. Der Zahlungsstatus enthält " Nicht gebuicht, unbezahlt, teilweise bezahlt und vollständig bezahlt.
Eine neue Rechnung aus einer Bestellung erstellen

Sie können eine neue Kreditorenrechnung erstellen, indem Sie die Aktivität **Neu** für den Arbeitsbereich **Kreditorenzusammenarbeitrechnungsstellung** auswählen. Die Bestellnummer und die Rechnungsnummer müssen vom Kreditor angegeben werden. Standardmäßig werden alle Positionen aus der Bestellung des neuen Kreditors auf der Rechnung angezeigt. Die Menge und die Kostendaten können vor dem Versenden der Kreditorenrechnung an den Workflow verarbeitet werden. Sie können Dateien, Hinweise, Bilder und URLs einer Rechnung zuordnen, bevor Sie diese senden.

Weitere Informationen finden Sie unter [Lieferantenzusammenarbeiten mit externen Kreditoren](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]