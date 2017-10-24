---
title: Dimensionsbasierte Produktkonfiguration
description: "Die dimensionenbasierte Produktkonfiguration stellt eine einfache Lösung für das Erstellen vieler Produktvarianten aus einem einzigen Produktmaster und seiner Stückliste dar."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e2ce0e95a5e1230df970b5d5249fdb248113cf54
ms.openlocfilehash: b6895726af6028035830893fdbb01a4a407d7076
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="dimension-based-product-configuration"></a>Dimensionsbasierte Produktkonfiguration

[!include[banner](../includes/banner.md)]


Die dimensionenbasierte Produktkonfiguration stellt eine einfache Lösung für das Erstellen vieler Produktvarianten aus einem einzigen Produktmaster und seiner Stückliste dar.

Die dimensionbasierte Produktkonfiguration ist eine von drei integrierten Produktkonfigurationstechnologien. Die beiden anderen Technologien sind vordefinierte Varianten und die einschränkungsbasierte Konfiguration. Alle drei Technologien verwenden einen Produktmaster als Ausgangspunkt und ermöglichen dem Benutzer, viele Produktvarianten für einen Produktmaster zu erstellen.

## <a name="key-concepts"></a>Schlüsselkonzepte
Die dimensionbasierte Produktkonfiguration basiert auf den folgenden Schlüsselkonzepten:

-   Produktmaster
-   Konfigurationsproduktdimension
-   Variantengruppen
-   Stücklisten
-   Variantenarbeitsplan
-   Variantenregeln

### <a name="product-masters"></a>Produktmaster

Ein Produktmaster ist der Ausgangspunkt für jeden Produktkonfigurationsprozess. Für die dimensionsbasierte Produktkonfiguration benötigen Sie einen Produktmaster mit eben dieser Konfigurationstechnologie und eine Produktdimensionsgruppe, die die Produktdimension der Konfiguration umfasst.

### <a name="configuration-product-dimension"></a>Konfigurationsproduktdimension

Die Produktdimension der Konfiguration wird dazu verwendet, die Produktvarianten für einen Produktmaster mithilfe der dimensionsbasierten Konfigurationstechnologie zu identifizieren. Der Konfigurationsdimensionswert wird vom Benutzer eingegeben und sollte helfen, die einzelnen Produktvarianten zu identifizieren.

### <a name="configuration-groups"></a>Variantengruppen

Variantengruppen werden in einem zentralen Repository definiert und können für alle dimensionsbasierten Produktkonfigurationsmodelle verwendet werden. Variantengruppen werden den einzelnen Stücklistenpositionen zugeordnet und halten eine Gruppe von Positionen zusammen, die sich gegenseitig ausschließen. Das bedeutet, dass lediglich eine Position in einer Gruppe für eine einzelne Produktvariante ausgewählt werden kann.

### <a name="bill-of-materials-bom"></a>Stücklisten

Die Stückliste stellt die Bausteine für eine dimensionsbasierte Produktkonfiguration dar. Sie muss alle verschiedenen Produkte enthalten, die in einer beliebigen Produktvariante verwendet werden können. Jede Position in der Stückliste kann auf eine Variantengruppe verweisen. Wenn eine Position nicht auf eine Variantengruppe verweist, wird sie in alle Produktvarianten einbezogen.

### <a name="configuration-route"></a>Variantenarbeitsplan

Der Variantenarbeitsplan bestimmt die Reihenfolge der Variantengruppen, also wie diese dem Benutzer während des Produktkonfigurationsprozesses angezeigt werden.

### <a name="configuration-rules"></a>Variantenregeln

Die Variantenregeln helfen sicherzustellen, dass ein Produkt, das in einer Variantengruppe in einer Stückliste enthalten ist, entweder eine Einbeziehung oder einen Ausschluss eines Produkts in einer anderen Variantengruppe in der gleichen Stückliste erzwingt.

## <a name="product-modeling-process"></a>Produktmodellprozess
Die natürliche Reihenfolge bei der Erstellung eines Produktmodells für ein dimensionsbasiertes Produkt beginnt mit dem Definieren der relevanten Variantengruppen. Es muss sichergestellt werden, dass alle Produkte, die in der Stückliste verwendet werden, für das Unternehmen freigegeben wurden, für das dieses Produktmodell erstellt wird. Mithilfe dieser Bausteine an vorhandenen Reservierungen für kann er die Stückliste erstellen und Variantengruppen zu den entsprechenden Stücklistenpositionen zuweisen. Wird in der Stückliste abgeschlossen ist, kann ein Variantenarbeitsplan für die Einrichtungen der Variantengruppen in der korrekten Reihenfolge definiert werden. [![Dimensionsbasiertes Produktmodellprozess](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Wenn es bestimmte Produkte von Gruppen die unterschiedliche Konfigurationsanforderungen gibt, die entweder nicht zusammen eingesetzt werden muss oder darf, Variantenregeln erstellen, können Sie die Produktbeziehungen diese erzwingen. Nachdem die Stückliste durch eine Stücklistenversion an einen dimensionsbasierten Produktmaster gebunden wurde und beide genehmigt und aktiviert wurden, können Sie Produktkonfigurationen erstellen und Namen für die einzelnen Konfigurationen eingeben. Die Konfigurationen können definiert werden, bevor eine Buchung generiert wird, oder sie werden definiert, wenn eine bestimmte Konfiguration erforderlich wird.

### <a name="suggested-use"></a>Verwendungsempfehlung

Die Technologie der dimensionsbasierten Konfiguration eignet sich insbesondere für Produkte mit begrenzter Variabilität, wenn die Kombination der Standardproduktdimensionen Größe, Farbe, Format und Konfiguration nicht für die Identifikation einer bestimmten Produktvariante geeignet ist. Ein Beispiel wäre ein Fahrrad mit Gestellgröße, Radgröße, Bremssystemen und unterschiedlichen Gängen.

### <a name="next-step"></a>Nächster Schritt 

Die folgenden acht Aufgabenleitfaden sind in diesem Thema in der Reihenfolge aufgeführt, in der Sie sie durchführen müssen. 

1.  [Dimensionsbasierten Produktmaster erstellen (Aufgabenleitfaden)](tasks/create-dimension-based-product-master.md)
2.  [Dimensionsbasierten Produktmaster freigeben (Aufgabenleitfaden)](tasks/release-dimension-based-product-master.md)
3.  [Grundeinrichtung eines freigegebenen Produktmasters abschließen (Aufgabenleitfaden)](tasks/complete-basic-setup-released-product-master.md)
4.  [Variantengruppen definieren (Aufgabenleitfaden)](tasks/define-configuration-groups.md)
5.  [Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen (Aufgabenleitfaden)](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Variantenarbeitspläne definieren (Aufgabenleitfaden)](tasks/define-configuration-route.md)
7.  [Variantenregeln erstellen (Aufgabenleitfaden)](tasks/create-configuration-rules.md)
8.  [Dimensionsbasierte Konfigurationen erstellen (Aufgabenleitfaden)](tasks/create-dimension-based-configurations.md)


