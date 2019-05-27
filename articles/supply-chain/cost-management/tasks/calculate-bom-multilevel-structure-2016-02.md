---
title: Berechnen einer Stückliste mithilfe einer Struktur mit mehreren Ebenen (Februar 2016)
description: Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit mehreren Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcc1248d64145c10f1c67bfac49c053e99dc1598
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557672"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Berechnen einer Stückliste mithilfe einer Struktur mit mehreren Ebenen (Februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit mehreren Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht. Es ist die siebente Aufgabe in der Stücklistenberechnungsserie. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.

1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Produkt-BOM_1 auswählen.  
3. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
4. Klicken Sie auf „Artikelpreis”.
5. Klicken Sie auf „Artikelkosten berechnen”.
    * Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.  
6. Geben Sie im Feld „Nachkalkulationsversion” einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Nachkalkulationsversion 20 aus, da sie ein Geplanter Kostentyp ist, und der Auflösungsmodus ist „Mehrere Ebenen”.   Der Auflösungsmodus „Mehrere Ebenen” ist für geplante Kosten und Simulationen. Er wird nicht für Standardkosten verwendet.  
7. Klicken Sie auf "OK".
8. Klicken Sie auf Berechnungsdetails anzeigen
    * Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.  In diesem Fall beachten Sie, wie BOM_2 berechnet wurde unter Berücksichtigung des Rohmaterials, Prozesses und des Mehraufwands mit einem Gesamtbetrag von 29,40 anstatt der Standardkosten von 10, die in dem ursprünglichen Aufgabenleitfaden in dieser Serie aktiviert wurden.  
9. Klicken Sie auf die Registerkarte „Nachkalkulationsbogen”.
    * Durch das Verschieben der Registerkarte „Nachkalkukationsbogen” sind die Summen pro Kostengruppe verschieden im Vergleich zur Berechnung, die im vorherigen Aufgabenleitfaden erfolgten.  
10. Wählen Sie im Feld „Ebene” die Option „Mehrere” aus.
    * Wenn Sie „Mehrfach” auswählen, werden die Kosten gemäß der Anordnung von BOM_2 klassifiziert, wobei 10 von der M1-Kostengruppe (ITEM_C) abgeleitet ist und 15,60 von der Produktion, wobei die Kostengruppe L2 beträgt. Indirekte Kosten variieren auch.  
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

