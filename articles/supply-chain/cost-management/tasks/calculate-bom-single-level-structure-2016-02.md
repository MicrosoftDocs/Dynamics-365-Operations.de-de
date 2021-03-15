---
title: Berechnen einer Stückliste mithilfe einer Struktur mit einfacher Ebene (Februar 2016)
description: Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit einer einzelnen Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f908e02c996c0d0a636fd9295b84fcc16b6b63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011771"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Berechnen einer Stückliste mithilfe einer Struktur mit einfacher Ebene (Februar 2016)

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit einer einzelnen Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht. Dies ist die sechste Aufgabe in der Stücklistenberechnungsserie. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.

1. Wechseln Sie zu "Freigegebene Produkte".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Produkt-BOM_1 auswählen.  
3. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
4. Klicken Sie auf „Artikelpreis”.
5. Klicken Sie auf „Artikelkosten berechnen”.
    * Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.  
6. Klicken Sie im Feld „Nachkalkulationsversion” auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie für diese Demo 10 aus. Dies ist die gleiche Nachkalkulationsversion, die zum Hinzufügen des Einstandspreis zu den Komponenten verwendet wird.  
7. Klicken Sie auf "OK".
8. Klicken Sie auf Berechnungsdetails anzeigen
    * Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.    Hier ist die Zusammenstellung der Kosten:   *    10 ist von ARTIKEL_A, 10 % von ARTIKEL_B, 10 % von BOM_2 berechnet. In diesem Fall gibt es keine Details für BOM_2, da sie als Standardkosten von 10 eingegeben wurde, aber es erfolgte nicht durch Berechnung.  *  7 ist von der Rüstzeit abgeleitet, welche konstante Kosten sind und zusätzliche 7 sind vom Laufzeitvorgang (Prozess) abgeleitet.  *   Es gibt auch andere Beträge, die den indirekten Kosten entsprechen.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]