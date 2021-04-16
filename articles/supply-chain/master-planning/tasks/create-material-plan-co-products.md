---
title: Erstellen Sie einen Materialplan für Co-Produkte
description: Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d910b89330865b0bcf3f6cd05b761506f339a45f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841670"
---
# <a name="create-a-material-plan-for-co-products"></a>Erstellen Sie einen Materialplan für Co-Produkte

[!include [banner](../../includes/banner.md)]

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
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Klicken Sie auf "Produktprogrammplanung".
4. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Beispiel: MasterPlan  
6. Klicken Sie auf "Ausführen".
7. Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.
8. Klicken Sie auf "Filter".
9. In der Liste wählen Sie die Zeile für Feld = Artikelnummer.
10. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Beispiel: P6003  
11. Klicken Sie auf "OK".
12. Klicken Sie auf "OK".
13. Klicken Sie auf "Bestellvorschläge".
14. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".
    * Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.  
15. Markieren Sie in der Liste die ausgewählte Zeile.
    * Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.  
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".
18. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.  
19. Schließen Sie die Seite.

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
1. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Beispiel: MasterPlan  
3. Klicken Sie auf "Ausführen".
4. Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.
5. Klicken Sie auf "Filter".
6. In der Liste wählen Sie die Zeile für Feld = Artikelnummer.
7. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Beispiel: P6003  
8. Klicken Sie auf "OK".
9. Klicken Sie auf "OK".
10. Klicken Sie auf "Bestellvorschläge".
11. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".
    * Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.  
12. Markieren Sie in der Liste die ausgewählte Zeile.
    * Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.  
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.  
16. Schließen Sie die Seite.
17. Klicken Sie auf "Produktprogrammplanung".
18. Wechseln Sie zu "Produktprogrammplan" > Einrichten > Produktprogrammplan-Parameter.
19. Wählen Sie im Feld "Alle Planungsprozessfelder deaktivieren" Nein aus.
20. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]