--- 
title: "Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen"
description: "Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f9f9473d0872d68571b87409b93e0cf5455364c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben. Die ersten 4 Aufzeichnungen richten Daten ein, die benötigt werden, um diese Prozedur abzuschließen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Aufgabe wird normalerweise vom Produktdesigner ausgeführt.


## <a name="select-the-product"></a>Wählen Sie das Produkt aus
1. Klicken Sie auf "Freigegebene Produktverwaltung".
2. Klicken Sie auf "Freigegebene Produkte".
3. Markieren Sie in der Liste die ausgewählte Zeile.
    * Suchen Sie den freigegebenen Produktmaster mit dimensionsbasierter Konfigurationstechnologie, die Sie im ersten Aufgabenleitfaden in dieser Sequenz erstellt haben.  
4. Klicken Sie im Aktivitätsbereich auf "Entwickler".
5. Klicken Sie auf "Stücklistenversionen".

## <a name="create-new-bom-and-bom-version"></a>Erstellen Sie neue Stückliste und Stücklistenversion
1. Klicken Sie auf "Neu".
2. Klicken Sie auf "Stückliste" und "Stücklistenversion".
3. Geben Sie im Feld "Name" einen Wert ein.
    * Festlegen eines Standorts  
    * In dieser Prozedur legen wir keinen bestimmten Standort für die Stückliste fest.  
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Neu".
    * In dieser Prozedur fügen wir vier Positionen der Stückliste hinzu. Zwei Positionen stellen Kabeloptionen dar und zwei Positionen stellen Gehäuseoptionen dar.  
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer "A0001", HDMI 6'-Kabel, aus.  
8. Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Kabelvariantengruppe aus, die im Leitfaden 4 in dieser Reihenfolge erstellt wird.  
9. Klicken Sie auf "Neu".
    * Wählen Sie Artikelnummer "A0002", HDMI 12'-Kabel, aus.  
10. Markieren Sie in der Liste die ausgewählte Zeile.
11. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
12. Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie erneut die Kabelvariantengruppe aus.  
13. Klicken Sie auf "Neu".
14. Markieren Sie in der Liste die ausgewählte Zeile.
15. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer "D0002 Gehäuse" aus.  
16. Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Gehäusevariantengruppe für diese Stücklistenposition aus.  
17. Klicken Sie auf "Neu".
18. Markieren Sie in der Liste die ausgewählte Zeile.
19. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer "M0007 StandardCabinet" als letzte Stücklistenposition aus.  
20. Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Gehäusevariantengruppe für die letzte Stücklistenposition aus.  

## <a name="approve-and-activate"></a>Genehmigen und aktivieren
1. Schließen Sie die Seite.
2. Klicken Sie auf Genehmigen.
3. Geben Sie im Feld 'Genehmig von' einen Wert ein, oder wählen Sie einen Wert aus.
4. Wählen Sie "Ja" aus in "Mächten Sie auch die Stückliste genehmigen?".
5. Klicken Sie auf "OK".
6. Klicken Sie auf Aktivieren.


