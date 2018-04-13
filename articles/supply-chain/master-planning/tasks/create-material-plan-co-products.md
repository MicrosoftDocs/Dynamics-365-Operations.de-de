--- 
title: "Materialplan für Co-Produkte erstellen"
description: "Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Materialplan für Co-Produkte erstellen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.


## <a name="create-requirement-for-a-co-product"></a>Anforderung für ein Co-Produkt erstellen
1. Wechseln Sie zu "Standard-Dashboard".
2. Klicken Sie auf "Auftragsverarbeitung und -abfrage".
3. Klicken Sie auf Neu.
4. Klicken Sie auf "Auftrag".
5. Geben Sie im Feld "Kundenkonto" einen Wert ein.
    * Beispiel: US-001  
6. Klicken Sie auf "OK".
7. Geben Sie im Feld "Artikelnummer" einen Wert ein.
    * Beispiel: P6003  
8. Geben Sie im Feld "Menge" eine Zahl ein.
    * Beispiel: 50000  
9. Klicken Sie auf "Speichern".

## <a name="create-a-material-plan-for-co-products"></a>Materialplan für Co-Produkte erstellen
1. Klicken Sie auf "Produktprogrammplanung".
2. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Beispiel: MasterPlan  
4. Klicken Sie auf "Ausführen".
5. Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.
6. Klicken Sie auf "Filter".
7. In der Liste wählen Sie die Zeile für Feld = Artikelnummer.
8. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Beispiel: P6003  
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".
11. Klicken Sie auf "Bestellvorschläge".
12. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".
    * Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.  
13. Markieren Sie in der Liste die ausgewählte Zeile.
    * Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.  
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
15. Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.  
17. Schließen Sie die Seite.


