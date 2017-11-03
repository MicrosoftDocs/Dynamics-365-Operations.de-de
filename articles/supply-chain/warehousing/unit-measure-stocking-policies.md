---
title: "Maßeinheit und Lagerrichtlinien"
description: "Dieser Artikel beschreibt, wie Standardmaßeinheiten, Einheitssequenzen und Einheitenumrechnungen in den Lagerortprozessen verwendet werden."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80bd5978ffe137e48da3f5eac6c75ad0f5e2f06a
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# Maßeinheit und Lagerrichtlinien

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt, wie Standardmaßeinheiten, Einheitssequenzen und Einheitenumrechnungen in den Lagerortprozessen verwendet werden.

Einheitensequenzgruppen definieren die Reihenfolge der Einheiten, die in den Lagerortarbeitsgängen verwendet werden können. Sie werden auf der Seite **Einheitensequenzgruppen** erstellt. Die Sequenz zeigt die Beziehung der verschiedenen Einheiten. Zum Beispiel speichern Sie Paletten, die Schachteln enthalten, die einzelne Artikel enthalten. In diesem Fall müssen Sie die drei verschiedenen Einheiten und die logische Reihenfolge der Ebenen bereitstellen. Mit Einheitssequenzgruppen können Sie die Richtlinien für die Gruppierung von Kennzeichen und die Standardmaßeinheiten definieren, die für die verschiedenen Lagerortverfahren verwendet werden sollen. Dieser Artikel gilt für die erweiterte Lagerungslösung, die in der Lagerortverwaltung verfügbar ist, sowie für die grundlegendere Lösung, die in der Bestandsverwaltung verfügbar ist.

## Einheitensequenzgruppen für freigegebene Produkte
Wenn Sie freigegebene Produkte in den Lagerortarbeitsprozessen verwenden möchten, muss eine Einheitensequenzgruppe zugewiesen werden. Wenn Sie ein Produkt überprüfen, das einer Lagerdimensionsgruppe zugeordnet ist, und die Option **Lagerortverwaltungsprozesse verwenden** für die Lagerdimensionsgruppe auf **Ja** festgelegt ist, erhalten Sie eine Fehlermeldung, wenn keine Einheitensequenzgruppenkennung für das Produkt definiert ist. Wenn die Einheitensequenzgruppe, die Sie verwenden, mehrere Positionen (und damit mehreren Einheiten) enthält, müssen Sie eine Einheitenumrechnung zwischen den Einheiten einrichten. Schließen Sie diese Einstellung auf der Seite **Einheitenumrechnungen** ab. Die kleinste Einheit in einer Sequenzgruppe, die Sie einem freigegebenen Produkt zuordnen, muss mit der Lagereinheit übereinstimmen, die für das entsprechende Produkt definiert ist. Die Lagereinheit ist die Einheit, die für Basisberechnungen des verfügbaren Lagerbestands verwendet wird. Sie können auch Maßeinheitsumrechnungen für Produktvarianten von Produktmastern einrichten, indem Sie die Option **Umrechnung von Maßeinheiten aktivieren** verwenden.

## Ladungsträgergruppierung
Sie können festlegen, ob Wareneingänge aus weniger oder mehr als einer bestimmten Einheit in einen Ladungsträger gruppiert werden oder in einen Ladungsträger für jede Einheit aufgeteilt werden sollen. Um das Verhalten einzurichten, verwenden Sie die Option **Ladungsträgergruppierung** auf der Registerkarte **Positionsdetails** der Seite **Einheitensequenzgruppen**. Wenn Sie Ladungsträgergruppierungen bei der Arbeit mit einem mobilen Gerät verwenden möchten, muss die Option **Ladungsträgergruppierung** im Menüelement **Mobiles Gerät** ausgewählt werden. Sie verwenden z. B. ein mobiles Gerät, um einen Artikel zu erfassen, der einer Einheitensequenzgruppe mit zwei Positionen zugeordnet ist. Die erste Position ist für Stücke und die Option **Ladungsträgergruppierung** ist auf **Ja** festgelegt. Die zweite Position ist für die Paletteneinheit und die Option **Ladungsträgergruppierung** ist auf **Nein** festgelegt. In diesem Fall kann das System die Teilung und die Erstellung von Kennzeichen pro 100 Stück automatisch verwalten.

## Einheiten für Zykluszählung
Um zu definieren, welche Einheiten als Teil der Zykluszählprozesse verwendet werden sollen, wählen Sie die Option **Einheit für Zykluszählung verwenden** auf der Seite **Einheitensequenzgruppen** aus. Sie können maximal vier Einheiten in der Nummernkreisgruppe auswählen. Wenn Sie mehr als vier Einheiten auswählen, werden die zusätzlichen Einheiten nicht im mobilen Gerät angezeigt.

## Standardeinheiten für den Empfang von Prozessen auf mobilen Geräten
Um die Standardeinheiten festzulegen, die für den Empfang von Prozessen auf mobilen Geräten verwendet werden sollen, aktivieren Sie die Optionen **Standardeinheit für Einkauf und Umlagerung** und **Standardeinheit für Produktion** auf der Seite **Einheitensequenzgruppen**. Beispielsweise können Sie angeben, dass das System standardmäßig Palettenmengen verwenden soll, wenn in einer Bestellung verfügbarer Lagerbestand unter Verwendung eines mobilen Geräts eingeht, die Lagermengeneinheit (LME) jedoch "Stück" sein soll. Um die Umrechnung für die Stückanzahl abzurufen, die jede Palette enthält, müssen Sie eine Einheitenumrechnung definieren, wie z. B. 100 Stck = 1 GuV.

## Standardauftragseinstellungen
Als Teil der Erstellung von freigegebenen Produkten müssen Sie Standardeinheiten für Einkäufe, Verkäufe und Lager auswählen, um die verschiedenen Aufträge zu verarbeiten. Sie können die Standardeinheiten und Mengen für die verschiedenen Quelldokumente mithilfe der Seiten **Standardauftragseinstellungen** und **Standortspezifische Auftragseinstellungen** festlegen. Sie können auf diese Seiten über die Seite **Freigegebene Produkte** zugreifen.




