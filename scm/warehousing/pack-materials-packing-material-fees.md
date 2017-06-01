---
title: "Verpackungsmaterial und Gebühren"
description: "Verpackungsmaterialgebühren werden in bestimmten Zeitabständen an ein Recyclingunternehmen entrichtet. Für jedes Material, aus dem eine Verpackung besteht, muss ein bestimmter Betrag pro Gewichtseinheit bezahlt werden. Verpackungsmaterialgebühren werden kalkuliert und erfasst, es werden jedoch keine Sachkontobuchungen ausgeführt, da die Gebühren nicht als Steuern betrachtet werden, die an eine Behörde zu entrichten sind."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e07ed8d8344576f96d2439051255d0e58555c30f
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="packing-materials-and-fees"></a>Verpackungsmaterial und Gebühren

[!include[banner](../includes/banner.md)]


Verpackungsmaterialgebühren werden in bestimmten Zeitabständen an ein Recyclingunternehmen entrichtet. Für jedes Material, aus dem eine Verpackung besteht, muss ein bestimmter Betrag pro Gewichtseinheit bezahlt werden. Verpackungsmaterialgebühren werden kalkuliert und erfasst, es werden jedoch keine Sachkontobuchungen ausgeführt, da die Gebühren nicht als Steuern betrachtet werden, die an eine Behörde zu entrichten sind.

Gewicht und Gebühren des Verpackungsmaterials werden sowohl für Bestell- als auch für Auftragspositionen ermittelt.

Sie können eine oder mehrere Verpackungseinheiten für einen Artikel, für eine Verpackungsgruppe oder für alle Artikel definieren. Eine Verpackungseinheit besteht neben der Anzahl der Artikel, die in der Verpackungseinheit enthalten sind, aus den verschiedenen Verpackungsmaterialien und ihrem jeweiligen Gewicht. Jedem definierten Typ von Verpackungsmaterial wird ein Verpackungsmaterialcode zugewiesen. Basierend auf dem Verpackungsmaterialcode, können Sie einen Preis für einen bestimmten Zeitraum angeben. Die Verpackungsmaterialgebühr wird anhand dieser Informationen berechnet.

| **Hinweis**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selbst wenn Ihr Unternehmen keine Verpackungsmaterialgebühren bezahlt, kann diese Funktion verwendet werden, um Statistiken für das Gewicht des Verpackungsmaterials zu ermitteln. |

## <a name="setup-requirements-for-packing-material-fees"></a>Einrichtungsanforderungen für Verpackungsmaterialgebühren
Bevor Sie Verpackungsmaterialgewichte oder -gebühren oder beides kalkulieren, müssen Sie die folgenden Stammdaten erstellen:

-   Verpackungsgruppen - Erstellen Sie Verpackungsgruppen, die Artikeln zugewiesen werden.
-   Verpackungsmaterialcodes - Erstellen Sie Verpackungsmaterialcodes für jeden Typ von Verpackungsmaterial, das definiert ist.
-   Verpackungseinheiten – Legen Sie eine Verpackungseinheit für einen Artikel, eine Verpackungsgruppe oder für alle Artikel fest. Für jede Verpackungseinheit legen Sie fest, welche Verpackungsmaterialien aufgenommen werden sollen, definieren Sie das Gewicht, und geben Sie im Feld "Verpackungseinheitenfaktor" den Umrechnungsfaktor von der Lagereinheit ein.
-   Verpackungsmaterialgebühren - Geben Sie Verpackungsmaterialgebühren für jeden Verpackungsmaterialcode an. Legen Sie für jeden Materialtyp den Gültigkeitszeitraum, den Preis pro Material, die Währung und die Einheit fest.

## <a name="packing-units-on-sales-order-lines"></a>Verpackungseinheiten in Auftragspositionen
Wenn Sie eine Auftragsposition erstellen, wird geprüft, ob für den Artikel Verpackungseinheiten festgelegt wurden. Wenn Verpackungseinheiten angegeben werden, aktualisiert das System die Auftragsposition mit der festgelegten Verpackungseinheit und der Menge der Verpackungseinheit. Zur Berechnung der Menge der Verpackungseinheit wird die bestellte Menge durch die Anzahl der Artikel in der gewählten Verpackungseinheit dividiert. Wenn keine Verpackungseinheit angegeben wurde, können Sie manuell für die Auftragsposition eine Verpackungseinheit und eine Verpackungseinheitenmenge eingeben. Es ist auch möglich, die Verpackungseinheit und die Verpackungseinheitenmenge beim Buchen der Auftragsposition zu ändern. Dies ist wichtig, wenn die Auftragsposition nur zum Teil geliefert oder zum Teil fakturiert wurde. Wenn der Auftrag fakturiert wird, werden Verpackungsmaterialbuchungen erstellt. Verpackungsmaterialbuchungen enthalten die Gewichtungen des Verpackungsmaterials für die Auftragsposition. Sie können die Buchungen auch ändern, nachdem Sie sie fakturiert haben, und anschließend neue Buchungen erstellen.

## <a name="packing-units-on-purchase-order-lines"></a>Verpackungseinheiten in Bestellpositionen
Verpackungsmaterialbuchungen für eine Bestellposition werden nicht vom System erstellt. Sie erstellen Buchungen für fakturierte Bestellpositionen manuell auf der Seite **Verpackungsmaterialbuchungen**.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Einrichten von Lizenznummern für Verpackungsmaterialgebühren bei Debitoren
Geben Sie im Formular **Debitoren** die Lizenznummer des Debitors für die Verpackungsmaterialgebühren an, wenn die Verpackungsmaterialgebühren durch den Debitor bezahlt werden. Wurde einem Debitor eine Lizenznummer zugeordnet, werden die Verpackungsmaterialgebühren automatisch beim Fakturieren von Aufträgen ermittelt. Nach der Fakturierung wird im Formular **Verpackungsmaterialbuchungen** das Kontrollkästchen **Gebühr berechnen** deaktiviert, da kein Bericht berechnet und gedruckt werden muss. Sie können das Gewicht des Verpackungsmaterials auf der Rechnung angeben und den Debitor darüber informieren, dass die Gebühren zu seinen Lasten gehen. 

Wenn die Verpackungsmaterialgebühren von Ihrem Unternehmen getragen werden, geben Sie keine Lizenznummern des Debitors an. Nach der Fakturierung wird das **Gebühr berechnen**-Kontrollkästchen auf der Seite **Verpackungsmaterialbuchungen** ausgewählt. Dadurch wird angegeben, dass die Gebühren beim Erstellen eines Berichts berechnet werden. Sie können das Gewicht auf der Rechnung angeben und darauf hinweisen, dass die Gebühren von Ihrem Unternehmen getragen werden.

## <a name="print-packaging-material-weights-on-invoices"></a>Angeben des Verpackungsmaterialgewichts auf Rechnungen
Sie können das Gewicht des Verpackungsmaterials auf der Rechnung ausweisen und angeben, wer für die aufgeführten Gebühren aufkommt. Das Gewicht wird nach Verpackungscode zusammengefasst.
 





