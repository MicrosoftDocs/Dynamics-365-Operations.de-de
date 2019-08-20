---
title: Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen
description: In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung in Dynamics 365 for Finance and Operations anpassen.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862613"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung in Dynamics 365 for Finance and Operations anpassen. Wenn das ursprüngliche Quelldokument verschiedene Steuerbeträge anzeigt, können Sie diese Beträge vor dem Buchen anpassen. Für diese Aufgabe wird das Demo-Unternehmen DEMF verwendet.

1. Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Name** der neuen Zeile eine Option im Dropdownmenü aus.
4. Wählen Sie im Aktivitätsbereich **Positionen** aus.
5. Geben Sie im Feld **Konto** die gewünschten Werte an.
6. Geben Sie im Feld **Rechnung** einen Wert ein.
7. Geben Sie im Feld **Kredit** eine Zahl ein.
8. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
9. Wählen Sie **Mehrwertsteuer** aus.
10. Geben Sie im Feld **Gesamter tatsächlicher Mehrwertsteuerbetrag** eine Zahl ein.
11. Auf der Registerkarte **Regulierung** können die Mehrwertsteuerbeträge pro Mehrwertsteuercode angepasst werden.
12. Wählen Sie **Istwerte aus berechneten Beträgen zurücksetzen** aus.
13. Wählen Sie **OK**.
14. Wählen Sie **Speichern**.

