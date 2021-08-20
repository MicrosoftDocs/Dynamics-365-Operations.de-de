---
title: Varianten für technische Produkte genieren
description: In diesem Thema wird beschrieben, wie Sie Varianten für technische Produkte generieren
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 57eda6a833df6ff8e91c006bbc5096554eff6c503a8b7ba2bd0b13e2f8e98f56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766146"
---
# <a name="generate-variants-for-engineering-products"></a>Varianten für technische Produkte genieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Varianten für technische Produkte generieren.

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Generieren Sie eine oder mehrere neue Varianten eines technischen Produkts

Sie können eine oder mehrere neue Varianten eines Produkts erstellen, ohne Informationen aus einem vorhandenen Produkt zu kopieren. Dies ist nützlich, wenn Sie mehrere Produktvarianten gleichzeitig erstellen müssen.

Das folgende Prozedur bietet ein Beispiel für die Erstellung mehrerer Varianten, die die Farbdimension enthalten.

1. Öffnen Sie die Seite **Freigegebene Produkte** (gehen Sie zum Beispiel zu **Verwaltung für technische Änderung \> Allgemein \> Freigegebene Produkte**).
1. Öffnen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** die Gruppe **Neu** und wählen Sie dann die Option **Technisches Produkt**.
1. Das Dialogfeld **Neues Produkt** wird geöffnet. Wählen Sie die passende **Technische Kategorie** aus.
1. Wenn Ihre ausgewählte technische Kategorie Variantendimensionen enthält, können Sie jetzt Werte dafür festlegen. In diesem Beispiel, können Sie, wenn die Kategorie eine Dimension **Farbe** hat, diese auf *Blau* einstellen.
1. Nehmen Sie nach Bedarf weitere Einstellungen vor. Wählen Sie **OK**, um das Produkt zu erstellen.
1. Das Produkt und die blaue Variante V-1 werden erstellt und das neue Produkt wird nun geöffnet.
1. Fügen Sie der Variante bei Bedarf eine Stückliste und einen Arbeitsplan hinzu.
1. Öffnen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Produktmaster** die Option **Produktdimensionen**.
1. Die Seite **Produktdimensionen** wird geöffnet. Diese Seite enthält eine Registerkarte für jede verfügbare Dimension. Fügen Sie auf jeder Registerkarte eine Zeile für jeden Wert hinzu, den Sie für jede relevante Dimension unterstützen. (In diesem Beispiel könnten Sie Zeilen in der Registerkarte **Farbe** für *Weiß*, *Gelb* und *Grün* zufügen).
1. Schließen Sie die Seite und wählen Sie **Freigegebene Produktvarianten**. Beachten Sie, dass die zuerst erstellte Variante (weißes V-1) angezeigt wird.
1. Wählen Sie **Variantenvorschläge** aus.
1. Das System schlägt Varianten mit den angelegten Farbwerten vor (z. B. weißes V-1, gelbes V-1 und grünes V-1).
1. Wählen Sie die vorgeschlagenen Varianten aus und wählen Sie **OK** aus, um die Varianten an das technische Unternehmen freizugeben. Beachten Sie, dass die folgenden Bedingungen gelten: 
    - Keine der erstellten Varianten hat eine Stückliste oder einen Arbeitsplan.
    - Die Attribute für diese Varianten stammen standardmäßig aus der technischen Kategorie und werden nicht aus der vorherigen Variante kopiert.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Eine Variante als Kopie einer anderen Produktvariante generieren

Sie können eine Variante eines Produkts basierend auf einer anderen Produktvariante erstellen. Die Stückliste und der Arbeitsplan aus der ursprünglichen Produktvariante werden in die neue Variante kopiert. Dies kann für Einzelfertigungen nützlich sein, bei denen es hilfreich sein kann, die Stückliste basierend auf einer ursprünglichen Stückliste zu erstellen und die Änderungen gegenüber der vorherigen Variante zu verfolgen. Um die Rückverfolgbarkeit zu wahren, zeichnet das System auf, welche Variante kopiert wurde, um eine neue Kopie anzulegen.

Das folgende Prozedur bietet ein Beispiel für das Erstellen einer neuen Variante, die die Farbdimension enthält, indem Sie eine Kopie einer vorhandenen Variante erstellen

1. Öffnen Sie die Seite **Freigegebene Produkte** (gehen Sie zum Beispiel zu **Verwaltung für technische Änderung \> Allgemein \> Freigegebene Produkte**).
1. Öffnen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** die Gruppe **Neu** und wählen Sie dann die Option **Technisches Produkt**.
1. Das Dialogfeld **Neues Produkt** wird geöffnet. Wählen Sie die passende **Technische Kategorie** aus.
1. Wenn Ihre ausgewählte technische Kategorie Variantendimensionen enthält, können Sie jetzt Werte dafür festlegen. In diesem Beispiel, können Sie, wenn die Kategorie eine Dimension **Farbe** hat, diese auf *Blau* einstellen.
1. Nehmen Sie nach Bedarf weitere Einstellungen vor. Wählen Sie **OK**, um das Produkt zu erstellen.
1. Das Produkt und die blaue Variante V-1 werden erstellt und das neue Produkt wird nun geöffnet.
1. Fügen Sie der Variante bei Bedarf eine Stückliste und einen Arbeitsplan hinzu.
1. Fügen Sie der Produktvariante bei Bedarf Attribute hinzu.
1. Fügen Sie einem technischen Änderungsauftrag die blaue Produktvariante V-1 hinzu.
1. Legen Sie **Auswirkung** auf *Neue Variante* fest.
1. Wählen Sie den neuen Farbwert aus (z. B. *Weiß*). Beachten Sie, dass die folgenden Bedingungen gelten: 
    - Die neue Variante hat eine Stückliste und einen Arbeitsplan, die aus der vorherigen Variante kopiert wurden.
    - Die neue Variante hat die von der vorherigen Variante kopierten Attribute.
1. Genehmigen Sie den Änderungsauftrag.
1. Verarbeiten Sie den Änderungsauftrag. Nach Verarbeitung des Auftrags wird die neue Variante V-1 erstellt und an das technische Unternehmen freigegeben.
