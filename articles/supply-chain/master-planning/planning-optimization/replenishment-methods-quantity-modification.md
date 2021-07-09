---
title: Methoden der Wiederbeschaffung und Mengenänderung
description: Dieses Thema enthält Informationen zu Wiederbeschaffungsmethoden in der Planungsoptimierung. Außerdem wird erklärt, wie die Mehrfachbestellmenge für ein Produkt das Ergebnis beeinflusst.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261695"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Methoden der Wiederbeschaffung und Mengenänderung

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Informationen zu Wiederbeschaffungsmethoden in der Planungsoptimierung. Außerdem wird erklärt, wie die Mehrfachbestellmenge für ein Produkt das Ergebnis beeinflusst.

Wiederbeschaffungsmethoden werden auch als Deckungsmethoden und Losgrößenmethoden bezeichnet.

## <a name="coverage-codes"></a>Abdeckungscodes

Die Planungsoptimierung kann für die Verwendung verschiedener Wiederbeschaffungsmethoden konfiguriert werden. Die Wiederbeschaffungsmethoden sind die Techniken, die das System verwendet, um den Bedarf für ein Produkt zu berechnen. Wiederbeschaffungsmethoden werden durch Abdeckungscodes definiert, die Sie entweder auf der Abdeckungsgruppe oder auf dem Produkt festlegen können.

Die folgenden Reichweitencodes können in der Planungsoptimierung verwendet werden:

- **Periode** – Die Wiederbeschaffungsmethode fasst den gesamten Bedarf für eine Periode in einem Auftrag für das Produkt zusammen. Der Auftrag wird für den ersten Tag der Periode geplant, und seine Menge erfüllt den Nettobedarf während des festgelegten Zeitraums. Die Periode beginnt mit dem ersten Bedarf des Produkts und umfasst die festgelegte Zeitspanne. Die nächste Periode beginnt mit dem nächsten Bedarf des Produkts. Der *Perioden*-Deckungscode wird häufig für nicht vorhersagbare Bestandsziehung, saisonabhängige Produkte oder Produkte mit hohen Kosten verwendet. Die folgende Abbildung zeigt ein Beispiel.

    ![Beispiel für die Verwendung des periodischen Abdeckungscodes](./media/coverage-code-period.png "Beispiel für die Verwendung des periodischen Abdeckungscodes")

- **Bedarf** – Bei der Wiederbeschaffungsmethode erstellt das System eine geplante Einkaufs-, Transport- oder Produktionsbestellung pro Bedarf für das Produkt. Diese Methode wird für teure Produkte verwendet, die einen intermittierenden Bedarf haben. Der *Bedarfsdeckungscode* wird häufig für konfigurierbare Produkte oder Make-to-Order-Szenarien verwendet. Die folgende Abbildung zeigt ein Beispiel.

    ![Beispiel für die Verwendung des Anforderungsabdeckungscodes](./media/coverage-code-requirement.png "Beispiel für die Verwendung des Anforderungsabdeckungscodes")

- **Min./Max.** - Die Methode der Wiederbeschaffung basiert auf dem Bestand. Sie definiert die Wiederbeschaffung des Bestands bis zu einem bestimmten Niveau, wenn der vorhergesagte Lagerbestand unter einem bestimmten Schwellenwert liegt. Die Wiederbeschaffungsmenge ist die Differenz zwischen dem maximalen Leven und dem Level der vorhergesagten Verfügbarkeit. Der *Min./Max.* Abdeckungscode wird häufig für vorhersagbare Bestandsentnahmen, hohe Läufer oder weniger teure Produkte verwendet. Die folgende Abbildung zeigt ein Beispiel.

    ![Beispiel für die Verwendung des Min./Max.Deckungscodes](./media/coverage-code-min-max.png "Beispiel für die Verwendung des Min./Max.Deckungscodes")

- **Manuell** – Bei der Wiederbeschaffung schlägt das System keine Einkaufs-, Transport- oder Produktionsaufträge für das Produkt vor. Stattdessen erstellt der Planer für das Produkt die erforderlichen Aufträge für die Wiederbeschaffung des Produkts. Der Deckungscode *Manuell* wird häufig für Produkte verwendet, für die systemgenerierte geplante Aufträge nicht erwünscht sind.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Auswirkung der Bestellmenge aus Standardauftragseinstellungen

Auf der Seite **Standardauftragseinstellungen** für ein freigegebenes Produkt können Sie jede der folgenden Mengeneinstellungen auf den Inforegistern **Einkaufsbestellung**, **Bestand** und **Verkaufsauftrag** festlegen. (Das Inforegister **Bestand** wird sowohl für Umlagerungsaufträge als auch für Fertigungsaufträge verwendet.)

- **Mehrfaches** – Geplante Aufträge werden ein Vielfaches dieser Menge sein.

    Wenn das Feld **Mehrfaches** zum Beispiel auf *5* festgelegt ist, kann ein Auftrag für eine Menge von 5, 10, 15, 20 usw. sein.

- **Min. Bestellmenge** – Geplante Aufträge werden nicht kleiner als der angegebene Wert sein.

    Wenn zum Beispiel das Feld **Min. Auftragsmenge** auf *10* festgelegt ist, wird ein geplanter Auftrag für eine Menge von 10 erstellt, auch wenn nur vier benötigt werden, um den Bedarf zu decken.

- **Max. Auftragsmenge** – Geplante Aufträge werden den angegebenen Wert nicht überschreiten. Ist der Bedarf größer als der Wert **Max. Auftragsmenge**, werden mehrere geplante Aufträge erstellt, um ihn zu decken.

    Wenn z. B. das Feld **Max. Auftragsmenge** auf *100* festgelegt ist und der Bedarf 450 beträgt, werden vier Planaufträge für eine Menge von 100 und ein Planauftrag für eine Menge von 50 erstellt.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Beispiele für die Wiederbeschaffung, die den Min./Max. Abdeckungscode

Wenn Sie auf der Seite **Standardauftragseinstellung** keinen Wert im Feld **Mehrfach** für ein Produkt festlegen und die *Min./Max.* Wiederbeschaffung verwenden, füllt die Planungsoptimierung den Bestand bis zu einer bestimmten Menge wieder auf, wenn der vorhergesagte Lagerbestand unter einem bestimmten Schwellenwert liegt.

Wenn Sie eine Mehrfachmenge für ein Produkt definieren, ändert die *Min./Max.* Wiederbeschaffung ihr Verhalten und berücksichtigt den **Mehrfachen** Wert.

Mit anderen Worten: Die Planungsoptimierung wird den Bestand auch dann bis zum definierten Maximalbestand wiederbeschaffen, wenn der vorhergesagte Lagerbestand kleiner als der definierte Minimalbestand ist. Die Wiederbeschaffung muss jedoch ein Vielfaches des **Vielfachen**-Wertes sein.

Wenn die Wiederbeschaffungsmenge (die Differenz zwischen dem Maximalbestand und dem vorhergesagten Lagerbestand) kein Vielfaches des definierten Vielfachen ist, verwendet die Planungsoptimierung den ersten möglichen Wert, der zusammen mit dem vorhergesagten Lagerbestand unter dem Maximalbestand liegt. Wenn die Summe kleiner als der Mindestbestand ist, verwendet die Planungsoptimierung den ersten Wert, der zusammen mit dem vorhergesagten Lagerbestand über dem Maximalbestand liegt.

In den folgenden Unterabschnitten finden Sie einige Beispiele, die zeigen, wie sich die Mehrfachbestellmenge für ein Produkt auf das Ergebnis der *Min./Max.* Wiederbeschaffung auswirkt.

### <a name="example-1"></a>Beispiel 1

Ein Produkt hat die folgende Konfiguration:

- **Deckungscode:** *Min./Max.*
- **Minimum:** *15*
- **Maximum:** *22*
- **Mehrfach:** *0*

Es gibt 10 Stück Lagerbestand für das Produkt, und es gibt keinen anderen Bedarf oder Vorrat.

Wenn die Produktprogrammplanung ausgeführt wird, wird ein geplanter Auftrag für 12 Stück erstellt, um den Bestand auf die maximale Menge aufzufüllen.

### <a name="example-2"></a>Beispiel 2

Ein Produkt hat die folgende Konfiguration:

- **Deckungscode:** *Min./Max.*
- **Minimum:** *15*
- **Maximal:** *22*
- **Mehrfach:** *5*

Es gibt 10 Stück Lagerbestand für das Produkt, und es gibt keinen anderen Bedarf oder Vorrat.

Wenn die Produktprogrammplanung ausgeführt wird, wird ein geplanter Auftrag über 10 Stück erstellt (weil 15 Stück Wiederbeschaffung plus 10 Stück Lagerbestand die Maximalmenge überschreiten).

### <a name="example-3"></a>Beispiel 3

Ein Produkt hat die folgende Konfiguration:

- **Deckungscode:** *Min./Max.*
- **Minimum:** *21*
- **Maximal:** *24*
- **Mehrfach:** *5*

Es gibt 10 Stück Lagerbestand für das Produkt, und es gibt keinen anderen Bedarf oder Vorrat.

Wenn die Produktprogrammplanung ausgeführt wird, wird ein geplanter Auftrag für 15 Stück erstellt (weil 10 Stück Wiederbeschaffung plus 10 Stück Lagerbestand weniger als die Mindestmenge sind).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
