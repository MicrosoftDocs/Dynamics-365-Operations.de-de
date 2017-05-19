---
title: "Arbeitsbereich für Kreditor-Kooperationsrechungen"
description: "In diesem Thema wird erläutert, wie Sie Kreditorenrechnungen anzeigen und Rechnungen vom Arbeitsberiech&quot;Kreditorenzusammenarbeit-Rechnungsstellung&quot; senden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7aebcdf0578d931d326420b42e2b220407049bc6
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-invoicing-workspace"></a>Arbeitsbereich für Kreditor-Kooperationsrechungen

[!include[banner](../includes/banner.md)]


In diesem Thema wird erläutert, wie Sie Kreditorenrechnungen anzeigen und Rechnungen vom Arbeitsberiech"Kreditorenzusammenarbeit-Rechnungsstellung" senden können.

Der Arbeitsbereich **Kreditor-Kooperationsrechnung** kann verwendet werden, um Kreditorenrechnungsinformationen anzuzeigen und Rechnungen an Microsoft Dynamics 365 für Arbeitsgänge mithilfe der Workflowfunktion zu senden.
Arbeitsbereich für Kreditor-Kooperationsrechungen
----------------------------------------

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die Kacheln **Zusammenfassung** bieten einen Überblick über die Rechnungen für den ausgewählten Kreditor. Sie können Rechnungen nach Status anzeigen.
-   Entwurfsrechnungen wurden nicht an den Workflow übermittelt.
-   Gesendete, nicht genehmigte Rechnungen sind jene Rechnungen, die vom Lieferanten übermittelt wurden, aber noch nicht in Dynamics 365 für Arbeitsgänge gebucht sind.
-   Genehmigte, nicht bezahlte Rechnungen sind jene Rechnungen, die im Dynamics 365 für Arbeitsgänge gebucht aber noch nicht vollständig bezahlt sind.
-   Bezahlte Rechnungen sind jene, die in Dynamics 365 für Arbeitsgänge vollständig bezahlt wurden.

Durch Klicken auf eine Kachel öffnet sich eine gefilterte Ansicht der Seite **Rechnungsliste**.
### <a name="tabular-lists"></a>Tabellarische Listen

Im Abschnitt **Tabellarische Listen**wird der Status der Rechnungsstellung auf ähnliche Weise aufgeteilt, wie die Zusammenfassung der Kacheln: Entwurfs- und übermittelte nicht genehmigte Listen. Im Entwurfstatus kann eine Rechnung an einen Workflow gesendet oder gelöscht werden. Die letzte tabellarische Liste ist eine Möglichkeit, Rechnungen zu suchen. Sie können Ihre Suche filtern, um schnellere Suchen zuzulassen.
Listenseite "Alle Kreditorenrechnungen"
-----------------------------

Sie können alle gebuchten und nicht gebuchten Kreditorenrechnungen auf der Listenseite **Kreditor-Kooperationsrechnungen** anzeigen. Sie können mit dieser Listenseite den Zahlungsstatus der Rechnungen anzuzeigen. Der Zahlungsstatus enthält " Nicht gebuicht, unbezahlt, teilweise bezahlt und vollständig bezahlt.
Eine neue Rechnung aus einer Bestellung erstellen
--------------------------------------------

Sie können eine neue Kreditorenrechnung erstellen, indem Sie die Aktivität **Neu** für den Arbeitsbereich **Kreditorenzusammenarbeitrechnungsstellung** auswählen. Die Bestellnummer und die Rechnungsnummer müssen vom Kreditor angegeben werden. Standardmäßig werden alle Positionen aus der Bestellung des neuen Kreditors auf der Rechnung angezeigt. Die Menge und die Kostendaten können vor dem Versenden der Kreditorenrechnung an den Workflow verarbeitet werden. Sie können Dateien, Hinweise, Bilder und URLs einer Rechnung zuordnen, bevor Sie diese senden.



Weitere Informationen finden Sie unter [Zusammenarbeiten mit Kreditoren mithilfe des Kreditorenportals](/dynamics365/operations/supply-chain/procurement/collaborate-vendors-vendor-portal)




