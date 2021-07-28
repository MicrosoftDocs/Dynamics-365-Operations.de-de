---
title: Dimensionsbasierte Produktkonfigurationen – Übersicht
description: Die dimensionenbasierte Produktkonfiguration stellt eine einfache Lösung für das Erstellen vieler Produktvarianten aus einem einzigen Produktmaster und seiner Stückliste dar.
author: cvocph
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 604b9e14d7a218ab75ebeff5b686f380ef88b34e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354688"
---
# <a name="dimension-based-product-configuration-overview"></a>Dimensionsbasierte Produktkonfigurationen – Übersicht

[!include [banner](../includes/banner.md)]

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
Die natürliche Reihenfolge bei der Erstellung eines Produktmodells für ein dimensionsbasiertes Produkt beginnt mit dem Definieren der relevanten Variantengruppen. Es muss sichergestellt werden, dass alle Produkte, die in der Stückliste verwendet werden, für das Unternehmen freigegeben wurden, für das dieses Produktmodell erstellt wird. Mithilfe dieser Bausteine an vorhandenen Reservierungen für kann er die Stückliste erstellen und Variantengruppen zu den entsprechenden Stücklistenpositionen zuweisen. Wird in der Stückliste abgeschlossen ist, kann ein Variantenarbeitsplan für die Einrichtungen der Variantengruppen in der korrekten Reihenfolge definiert werden. [![Dimensionsbasierter Produktmodellprozess.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Wenn es bestimmte Produkte von Gruppen die unterschiedliche Konfigurationsanforderungen gibt, die entweder nicht zusammen eingesetzt werden muss oder darf, Variantenregeln erstellen, können Sie die Produktbeziehungen diese erzwingen. Nachdem die Stückliste durch eine Stücklistenversion an einen dimensionsbasierten Produktmaster gebunden wurde und beide genehmigt und aktiviert wurden, können Sie Produktkonfigurationen erstellen und Namen für die einzelnen Konfigurationen eingeben. Die Konfigurationen können definiert werden, bevor eine Buchung generiert wird, oder sie werden definiert, wenn eine bestimmte Konfiguration erforderlich wird.

### <a name="suggested-use"></a>Verwendungsempfehlung

Die Technologie der dimensionsbasierten Konfiguration eignet sich insbesondere für Produkte mit begrenzter Variabilität, wenn die Kombination der Standardproduktdimensionen Größe, Farbe, Format und Konfiguration nicht für die Identifikation einer bestimmten Produktvariante geeignet ist. Ein Beispiel wäre ein Fahrrad mit Gestellgröße, Radgröße, Bremssystemen und unterschiedlichen Gängen.

### <a name="next-step"></a>Nächster Schritt 

Die folgenden acht Aufgabenleitfaden sind in diesem Thema in der Reihenfolge aufgeführt, in der Sie sie durchführen müssen. 

1.  [Dimensionsbasierten Produktmaster erstellen](tasks/create-dimension-based-product-master.md)
2.  [Dimensionsbasierten Produktmaster veröffentlichen](tasks/release-dimension-based-product-master.md)
3.  [Grundeinrichtung eines veröffentlichten Produktmasters abschließen](tasks/complete-basic-setup-released-product-master.md)
4.  [Variantengruppen definieren](tasks/define-configuration-groups.md)
5.  [Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Variantenarbeitspläne definieren](tasks/define-configuration-route.md)
7.  [Variantenregeln erstellen](tasks/create-configuration-rules.md)
8.  [Dimensionsbasierte Konfigurationen erstellen](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]