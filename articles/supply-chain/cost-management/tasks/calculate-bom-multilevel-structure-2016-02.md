--- 
title: "Berechnen einer Stückliste mithilfe einer Struktur mit mehreren Ebenen (nur Februar 2016)"
description: "Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit mehreren Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Berechnen einer Stückliste mithilfe einer Struktur mit mehreren Ebenen (nur Februar 2016)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


