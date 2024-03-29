---
title: Chargenattribute
description: Dieser Artikel enthält Informationen zu Chargenattributen. Chargenattribute sind Merkmale von Rohmaterialien und Fertigprodukten, aus denen sich die Lagerchargen zusammensetzen. Der Artikel beschreibt ausserdem, wie Chargenattribute zugeordnet und wie sie durchsucht werden können, wenn Sie Chargen reservieren.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5f5a03df63cf4fa90b5e9e67082a0d60eef9afc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899381"
---
# <a name="batch-attributes"></a>Chargenattribute

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Chargenattributen. Chargenattribute sind Merkmale von Rohmaterialien und Fertigprodukten, aus denen sich die Lagerchargen zusammensetzen. Der Artikel beschreibt ausserdem, wie Chargenattribute zugeordnet und wie sie durchsucht werden können, wenn Sie Chargen reservieren.

Chargenattribute sind Merkmale von Rohmaterialien und Fertigprodukten, aus denen sich die Lagerchargen zusammensetzen. Chargenattribute können sich abhängig von verschiedenen Faktoren unterscheiden, wie etwa den Umgebungsbedingungen, der Qualität des für die Produktion der Charge verwendeten Rohmaterials oder des Ergebnisses des fertigen Produkts. Die Anzahl und Typen der verwendeten Chargenattribute sind stark branchenabhängig. Nachfolgend finden Sie zwei Beispiele zur Verwendung von Chargenattributen:

-   Bei der Käseherstellung werden der Milch als einem der Rohstoffe zur Herstellung von Käse Attribute wie Fettgehalt und Gewichtsanteil des Fetts in Prozent zugeordnet. Dem mithilfe der Milch hergestellten Käse können zusätzliche Attribute wie Feuchtigkeit und Alter zugeordnet werden.
-   In der stahlverarbeitenden Industrie besitzt das produzierte Eisen möglicherweise Attribute wie die prozentualen Magnesium-, Silber- und Zinkanteile.

Um die Anzahl und Typen von Attributen besser zu verwalten, können Sie Chargenattributgruppen verwenden. Auf diese Weise müssen Sie nicht jedes Attribut einzeln hinzufügen.

## <a name="assign-batch-attributes"></a>Zuweisen von Chargenattributen
Chargenattribute können einzelnen Produkten, die sich in Lagerchargen befinden, oder Produkten zugewiesen werden, die bestimmten Debitoren zugeordnet sind. Ein Chargenattribut kann erst auf Debitorenebene zugeordnet werden, wenn es auf Produktebene zugewiesen wurde. Für das Produkt muss die Chargendimension in der Rückverfolgungsangabengruppe **Aktiv** festgelegt werden. Weisen Sie ein Chargenattribut zu einem einzelnen Produkt mithilfe der produktspezifischen Seite zu. Ist das Attribut spezifisch für ein Produkt eines Debitors, verwenden Sie die debitorenspezifische Seite. Beim Hinzufügen eines Attributs zu einem Produkt legen Sie außerdem folgende Parameter fest. Nachfolgend finden Sie einige Beispiele:

-   Die Bereiche für Mindest- und Höchstwerte für ein Attribut vom Typ **Ganze Zahl** oder **Bruch**.
-   Die Toleranzaktionen für Attribute vom Typ **Ganze Zahl** oder **Bruch**. Die von Ihnen ausgewählte Aktivität kann eine Warnmeldung oder eine Fehlermeldung sein, falls das Attribut nicht im Bereich für Mindest- und Höchstwerte liegt.
-   Der Zielwert des Attributs. Dieser Wert ist der optimale Wert des Attributs. Er gilt für alle Attributtypen.

Sie können auf diese Seiten für Produkte zugreifen, die Sie auf der Seite **Freigegebene Produkte** unter Produktinformationsverwaltung auswählen. Nach dem Zuweisen von Chargenattributen zu einem Produkt können Sie den Attributen auf der Seite **Lagerchargenattribute** bestimmte Werte hinzufügen.

## <a name="reserve-batches"></a>Reservieren von Chargen
Sie können nach Chargenattributen suchen, wenn Sie Stapelreservierungen zur Erfüllung eines Debitorenauftrags vornehmen oder wenn Sie Chargen für einen Produktionsauftrag entnehmen und reservieren. Mit dieser Suche können Sie eine Lagercharge ausfindig machen, die das Produkt mit den gewünschten Chargenattributen enthält. Nachdem Sie die Charge oder Chargen gefunden haben, können Sie das Produkt in der erstellten Lagerbuchungsposition reservieren.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]