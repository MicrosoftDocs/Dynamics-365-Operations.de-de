---
title: Materialentnahme berechnen
description: Dieser Artikel enthält Informationen zu unterschiedlichen Optionen, die in Zusammenhang mit der Berechnung des Materialverbrauchs stehen.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f58365278200344169b93658e9c92dea2bc4f18f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211632"
---
# <a name="calculate-material-consumption"></a>Materialentnahme berechnen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu unterschiedlichen Optionen, die in Zusammenhang mit der Berechnung des Materialverbrauchs stehen. 

Die folgenden Optionen, die mit der Berechnung des Materialverbrauchs zusammenhängen, sind auf den Registerkarten **Einstellungen** und **Verbrauch pro Schritt** auf dem Inforegister **Positionsdetails** der Seite **Stücklisten** verfügbar.

## <a name="variable-and-constant-consumption"></a>Variabler und konstanter Verbrauch
Im Feld **Verbrauch** können Sie auswählen, ob der Verbrauch auf konstanten Mengen oder auf variablen Mengen berechnet werden soll. Wählen Sie **Konstant**  wenn eine feste Menge oder ein festes Volumen benötigt wird, und zwar unabhängig von der produzierten Menge. Wählen Sie **Variable** aus, was die Standardeinstellung ist, wenn die erforderliche Menge des Materials in den fertigen Waren im Verhältnis zur Anzahl der fertigen Waren steht, die produziert werden.

## <a name="calculating-consumption-from-a-formula"></a>Verbrauch nach einer Formel berechnen
Im Feld **Formel** können Sie verschiedene Formeln für die Berechnung des Materialverbrauchs einrichten. Wenn Sie den Standardwert **Standard** verwenden, wird der Verbrauch nicht nach einer Formel berechnet. Die folgenden Formeln funktionieren zusammen mit den Feldern **Höhe**, **Breite**, **Tiefe**, **Dichte** und **Konstante**:

-   Höhe \* Konstante
-   Höhe \* Breite \* Konstante
-   Höhe \* Breite \* Tiefe \* Konstante
-   (Höhe \* Breite \* Tiefe/Dichte) \* Konstante

## <a name="rounding-up-and-multiples"></a>Aufrunden und Vielfache
Zusammen ermöglichen Ihnen die Felder **Aufrunden** und **Vielfache**, den Materialverbrauchswert aufzurunden. So können Sie beispielsweise den Wert entsprechend der Handhabungseinheit aufrunden, in der das Rohmaterial für die Produktion entnommen wird. Die folgenden Optionen stehen im Feld **Aufrunden** zur Verfügung: **Menge**, **Messung** und **Verbrauch**.

### <a name="quantity"></a>Menge

Wenn Sie **Menge** als Aufrundungsmechanismus auswählen, muss die Menge ein Mehrfaches der angegebenen Menge sein. Wenn z. B. ganze Zahlen erforderlich sind, wählen Sie den Wert **1** im Feld **Vielfaches** aus. Zahlen werden dann zu einer Menge aufgerundet, die durch 1 teilbar ist.

### <a name="measurement"></a>Verbrauchsberechnung

In der Regel wählen Sie **Messung** als Aufrundungsmechanismus aus, wenn das Rohmaterial in bestimmten Abmessungen geliefert wird. Beispielsweise ist ein Stück eines 2-Meter-Metallrohrs für eine fertige Ware erforderlich, und das Metallrohr wird in Längen von 4,5 Metern gelagert. In diesem Fall kann der Aufrundungsmechanismus **Messung** verwendet werden, um zu berechnen, wie viele Metallrohre erforderlich sind, um eine bestimmte Stückanzahl fertige Ware zu erzeugen. Bei diesem Beispiel wird das Feld **Formel** auf festgelegt **Höhen\*Konstante** festgelegt. Das Feld **Höhe** wird auf **2** festgelegt, um die Länge des Rohrs anzugeben, das für das Endprodukt erforderlich ist. Das Feld **Mehrfach** wird auf **4,5** festgelegt, um anzugeben, dass das Rohr in Längen von 4,5 Metern entnommen wird. Hier ist die Berechnung:

1.  Anzahl der Vielfachen, die für 10 Stück der fertigen Ware erforderlich sind: 10 ÷ 2 = 5 Stück
2.  Gesamtverbrauch: 4,5 × 5 = 22,5 Meter des Metallrohrs

Es wird angenommen, dass 0,5 Meter des Rohrs für alle fünf Stücke des Rohrs verschrottet werden, die verbraucht werden.

### <a name="consumption"></a>Verbrauch

In der Regel wählen Sie**Verbrauch** als Aufrundungsmechanismus aus, wenn Rohmaterial in gesamten Mengen einer bestimmten Handhabungseinheit des Produkts entnommen werden muss. Beispielsweise werden 2 Liter Farbe verwendet, die zur Produktion einer fertigen Ware verwendet werden, und die Farbe wird in 25-Liter-Eimern entnommen. In diesem Fall kann der Aufrundungsmechanismus **Verbrauch** verwendet werden, um den Verbrauch auf ganze Anzahlen von 25-Liter-Eimern aufzurunden. Ist hier die Berechnung für die benötigte Farbmenge, wenn 180 Stück fertige Ware produziert werden müssen:

1.  Farbe, die erforderlich ist, abzüglich des Ausschusses: 180 × 2 = 360 Liter
2.  Anzahl der Farbeimer: 360 ÷ 25 = 14,4, das auf 15 aufgerundet wird
3.  Farbe, die erforderlich ist, einschließlich des Ausschusses: 15 × 25 = 375 Liter

## <a name="step-consumption"></a>Verbrauch pro Serie
"Verbrauch pro Schritt" wird verwendet, um den konstanten Verbrauch in Mengenintervallen zu berechnen. Wenn Sie **Verbrauch pro Schritt** im Feld **Berechnungsgrundlage** auf der Registerkarte **Einstellungen** auswählen, können Sie Informationen über die Schritte auf der Registerkarte **Verbrauch pro Schritt** hinzugefügt. Die feste verbrauchten Menge kann in die Intervalle der hergestellten Menge eingerichtet werden. Beispielsweise wird der Verbrauch pro Schritt, wie in der folgenden Tabelle angezeigt, eingerichtet.

| Von Serie | Menge |
|-------------|----------|
| 0,00        | 10.0000  |
| 100,00      | 20.0000  |
| 200,00      | 40.0000  |

Die Stücklistenmenge (BOM) ist 1 und die Produktionsmenge ist 110. Die Formel für den Verbrauch ist "Von Serien (Menge) = Verbrauch. Da die Produktionsmenge 110 ist, fällt sie in die "Von-100-Serie". Die Menge ist daher 20.



