---
title: Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen
description: In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung in Dynamics 365 Finance anpassen.
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
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139966"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung anpassen. Wenn das ursprüngliche Quelldokument verschiedene Steuerbeträge anzeigt, können Sie diese Beträge vor dem Buchen anpassen. Für diese Aufgabe wird das Demo-Unternehmen DEMF verwendet.

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

