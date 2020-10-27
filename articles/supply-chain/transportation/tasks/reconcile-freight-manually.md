---
title: Fracht manuell abstimmen
description: Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b466db6d0568918b0833cc28e32c33168fac814
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978312"
---
# <a name="reconcile-freight-manually"></a>Fracht manuell abstimmen

[!include [banner](../../includes/banner.md)]]

Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird. Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.


## <a name="select-a-load-to-reconcile"></a>Eine Auslastung zur Abstimmung auswählen
1. Wechseln Sie zu Transportverwaltung > Planung > Ladungsplanungsworkbench.
2. Deaktivieren Sie das Kontrollkästchen "'Versendet' und 'Empfangen' ausblenden". 
3. In der Liste wählen Sie die Auslastung aus, die die Auslastungskennung 00006 hat.

## <a name="create-a-carrier-invoice"></a>Erstellen einer Spediteursrechnung
Wenn Sie Fracht manuell abstimmen und nicht automatischen Spediteursrechnungen empfangen, können Sie eine Rechnung auf Basis des Frachtbriefs erstellen.  
1. Klicken Sie auf "Zugehörige Informationen".
2. Klicken Sie auf Frachtbriefdetails.
3. Klicken Sie auf "Frachtbriefrechnung generieren".
4. Geben Sie im Feld "Rechnung" einen Wert ein.
5. Klicken Sie auf "OK".

## <a name="reconcile-the-invoice"></a>Rechnung abstimmen
Wenn Sie eine Spediteursrechnung und einen Frachtbrief abstimmen, passiert dies Position für Position.  
1. Klicken Sie auf "Frachtbriefe und Rechnungen abgleichen".
2. Erweitern Sie den Abschnitt "Rechnungsdetails".
3. Erweitern Sie den Abschnitt "Nicht abgeglichene Frachtbriefdetails".
4. Markieren Sie in der Liste die ausgewählte Zeile.
5. Klicken Sie auf "Abgleichen".
6. Erweitern Sie den Abschnitt "Abgeglichene Frachtbriefdetails".

## <a name="submit-the-invoice-for-approval"></a>Rechnung zur Genehmigung übermitteln
1. Klicken Sie auf "Zur Genehmigung senden".
2. Schließen Sie die Seite.
3. Deaktivieren Sie das Kontrollkästchen 'Ausblenden genehmigt'. 
4. Klicken Sie auf Kreditorenrechnungserfassungen
5. Klicken Sie, um dem Link im Feld "Referenzerfassungsnummer".
6. Klicken Sie auf "Positionen".

