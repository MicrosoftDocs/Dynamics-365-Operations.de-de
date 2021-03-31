---
title: Sachkonto-Zuordnungserfassung verarbeiten
description: In diesem Thema wird erläutert, wie Sie unter Dynamics 365 Finance eine Zuordnungsanforderung bearbeiten.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a52a5ce2d789757a11c9e443c7f25058bd9d8a91
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222334"
---
# <a name="process-ledger-allocation-journal"></a>Sachkonto-Zuordnungserfassung verarbeiten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine Zuordnungsanforderung bearbeiten. Mithilfe der Seite "Zuordnungsanforderung verarbeiten" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann. Vor der Erstellung einer Zuordnungserfassung muss mindesten eine Sachkontozuordnungsregel erstellt werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Zuordnungen > Prozessverrechnungsanforderung**.
2. Wählen Sie im Feld **Regel** den gewünschten Datensatz im Dropdown-Menü aus.
3. Geben Sie im Feld **Als Datum** ein Datum ein.

    - Das **Als Datum** ist sehr wichtig, wenn das Ledger die Datenquelle für die Regel ist. Dieses Datum steuert, welche Sachkonto für die Zuweisung genutzt wird.  
    - Im Feld **Nullquelle** wählen Sie **Stop**. Dadurch wird der Zuordnungsprozess gestoppt und eine Meldung angezeigt, die besagt, dass ein Betrag von Null ausgewählt wurde.  

4. Wählen Sie im Feld **Vorschlagsoptionen** **Nur Vorschlag**. Wählen Sie **Nur Vorschlag**, um das Ergebnis in Allokationsbüchern zu überprüfen und optional zu genehmigen, bevor Sie die Allokation ins Hauptbuch buchen.  
5. Geben Sie im Feld "Datum für Sachkontobuchung" ein Datum ein.
6. Wählen Sie **OK**.
7. Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Zuordnungen > Zuordnungen > Zuordnungsjournale**.
8. Wählen Sie **Positionen** aus.
9. Wählen Sie **Buchen** aus.
10. Wählen Sie **Buchen** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]