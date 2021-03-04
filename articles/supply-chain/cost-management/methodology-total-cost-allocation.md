---
title: Gesamtkostenzuteilungsmethode
description: Dieser Artikel zeigt die Richtlinien für die Verwendung der Gesamtkostenzuteilung auf. Gesamtkostenzuteilung ist eine Methode zur Berechnung der Kosten zwischen dem Hauptformelartikel für einen Chargenauftrag und den Kuppelprodukten, die für die Formel definiert werden.
author: AndersGirke
manager: tfehr
ms.date: 04/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 758015c566e39df7306e1b34b8d3b42f1f1eba79
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428457"
---
# <a name="total-cost-allocation-method"></a>Gesamtkostenzuteilungsmethode

[!include [banner](../includes/banner.md)]

Gesamtkostenzuteilung (TCA) ist eine Methode zur Berechnung der Kosten zwischen dem Hauptformelartikel für einen Chargenauftrag und den Kuppelprodukten, die für die Formel definiert werden. Diese Methode ist dynamisch. Es werden die Kosten als gewichteter Durchschnitt der Mengen, die für die Formelartikel und Kuppelprodukte als fertig gemeldet werden, berechnet. Wenn die Gesamtkostenzuweisung verwendet wird, müssen Sie nicht für jeden Chargenauftrag Kostenzuweisungen überprüfen. Wenn die Gesamtkostenzuweisung nicht verwendet wird, verwendet die Formelberechnung vorhandene Funktionen.

## <a name="using-tca-for-coproducts"></a>Verwenden der Gesamtkostenzuweisung für Kuppelprodukte
Im Folgenden sehen Sie einige der Richtlinien für die Verwendung von Gesamtkostenzuweisungen für Kuppelprodukte:

-   Wenn Sie den Schieberegler **Gesamtkostenzuweisung** auf **Ja** für eine Formelversion festlegen, muss der Einstandspreis für Kuppelprodukte mehr als 0 (null) betragen. Der Wert kann aus der Version der aktiven Kosten des selben Standorts oder für den ersten Standort einer Formel, die nicht standortspezifisch ist, abgerufen werden. Diese Bedingung wird geprüft, wenn die Formel genehmigt wurde.

    -   Sie müssen die Kostenzuteilungsprozentsätze für Kuppelprodukte nicht manuell eingeben. Stattdessen erstellt das System automatisch den Kostenzuweisungsprozentsatz als Durchschnitt der aktiven Kosten von Kuppelprodukten. 
    -   Sie müssen die Standardkosten für nichtstandardisierte Kostenfaktoren, die Kuppelprodukte sind, nicht eingeben. Es gibt zwei Typen von Kostenversionen im System: Standardkosten und geplante Kosten 
    -   Wenn ein Artikel nicht von der Standardkostenbewertungsmethode bewertet wird, empfehlen wir Ihnen, einen aktiven Kostenpreis in der geplanten Version zu berücksichtigen. Dieser Preis wird für die Vorkalkulation verwendet, beispielsweise für Stücklistenkalkulation,  Produktionskostenvorkalkulation und Herstellkostenkalkulation, und Fallback-Preis im Lagerbewertungsprozess. 

-   Wenn Sie den Schieberegler **Gesamtkostenzuweisung** auf **Ja** für die Formelversion festlegen und die folgenden Bedingungen zutreffen, ist die Methode der Kostenzuweisung **Gesamtkostenzuweisung**, und der Prozentsatz der Kostenzuweisung wird nicht geändert:
    -   Sie haben Kuppelprodukte hinzugefügt.
    -   Sie haben eine andere Methode der Kostenzuweisung für die Kuppelprodukte verwendet.
-   Wenn Sie den Schieberegler **Gesamtkostenzuweisung** auf **Nein** für die Formelversion festlegen und die folgenden Bedingungen zutreffen, ändert sich die Methode der Kostenzuweisung auf **Manuell**, und der Prozentsatz der Kostenzuweisung wird nicht geändert:
    -   Sie haben Kuppelprodukte hinzugefügt.
    -   Der Prozentsatz der Kostenzuweisung ist größer als 0 (Null).
-   Bevor Sie eine Formelberechnung erfolgreich ausführen können, müssen Sie die Prozentsätze der Kostenzuweisung kalkulieren. Sie können diesen Schritt manuell abschließen oder indem Sie die Option **Kosten vorkalkulieren** auf der Seite **Kuppelprodukte** verwenden. **Hinweis:** Die Option **Kosten vorkalkulieren** ist nur verfügbar, wenn der Schieberegler **Gesamtkostenzuweisung** für die Formelversion auf **Ja** festgelegt ist. Sie können die erwartete Zuteilung anzeigen, wenn die als fertig gemeldeten Chargenauftragsmengen, den Mengen entsprechen, die in der Formel angezeigt werden.
-   Wird ein Chargenauftrag manuell erstellt oder ein geplanter Chargenauftrag umgewandelt, wird der Wert des Schiebereglers **Gesamtkostenzuweisung** der Formelversion in den Chargenauftrag kopiert. Sie können diese Einstellung im Chargenauftrag ändern. Wenn der Schieberegler **Gesamtkostenzuweisung** für die Formelversion auf **Nein** festgelegt ist und anschließend für den Chargenauftrag auf **Ja** geändert wird, wird die Methode der Kostenzuweisung für jede Position, die auf **Manuell** festgelegt wurde, auf **Gesamtkostenzuweisung** geändert. Eine Kostenzuweisung von **Keine** bleibt unverändert. Wenn der Schieberegler **Gesamtkostenzuweisung** auf **Ja** für die Formelversion festgelegt ist und anschließend für den Chargenauftrag auf **Nein** geändert wird, wird die Methode der Kostenzuweisung für jedes Kuppelprodukt des Typs **Produktion** auf **Manuell** geändert. Jeder vorkalkulierte Prozentsatz der Kostenzuweisung bleibt unverändert.
-   Die Seite **Kostenzuweisung für Kuppelprodukte** zeigt die berechnete Kostenzuweisung in Prozent an. Sie können diese Seite über die Seite **Chargenauftrag** öffnen. Diese Information ist hilfreich, wenn die gemeldeten Produkte und Mengen von den geplanten oder gestarteten Mengen des Chargenauftrags abweichen. Wenn die Kosten vollständig sind, werden diese neuen Prozentsatzzuweisungen aus der Gesamtkostenzuweisung auf der Seite **Kostenzuteilung für Kuppelprodukte** angezeigt.

## <a name="calculating-the-burden-for-byproducts"></a>Berechnen der Gemeinkosten für Nebenprodukte
Das Feld **Nebenproduktkostenzuweisung** auf der Seite **Kuppelprodukte** ist ein Enumeratorfeld, das nur für Nebenprodukte verwendet wird. Für Kuppelprodukte ist der Wert dieses Felds immer **Keine**. Für Nebenproduktpositionen legt dieses Feld fest, wie der Kostenbetrag für die Nebenproduktposition zu den Gesamtkosten der Produktion hinzugefügt wird. Die folgenden Optionen sind verfügbar:

-   **Kein** ─ Kein Betrag wird in die Gesamtkosten der Produktion dieser Nebenproduktposition hinzugefügt.
-   **Prozent** ─ Der Einstandsbetrag wird als Prozentsatz der Gesamtkosten der Rohmaterialien berechnet, die bei der Produktion verbraucht werden. Der Prozentsatz, der für die Berechnung der Quellensteuer verwendet wird, wird im Feld eingegeben.
-   **Pro Serie** ─ Der Einstandsbetrag wird als Betrag pro Standardchargengröße des Produktionsauftrags berechnet. Dieser Betrag ist unabhängig von der gemeldeten Menge in der Produktion. Der Betrag, der für die Berechnung verwendet wird, wird im Feld eingegeben.
-   **Nach Menge** ─ Der Einstandsbetrag wird als Betrag pro gemeldeter Menge des Formelartikels in der Produktion berechnet. Der Betrag, der für die Berechnung verwendet wird, wird im Feld eingegeben.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]