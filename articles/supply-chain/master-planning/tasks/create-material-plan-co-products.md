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
ms.openlocfilehash: d829687521c002a84de8f88caff22a8f0362c75e91ac355fd0b5002d0bd981c2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768070"
---
# <a name="create-a-material-plan-for-co-products"></a>Erstellen Sie einen Materialplan für Co-Produkte

[!include [banner](../../includes/banner.md)]

Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.

## <a name="create-requirement-for-a-co-product"></a>Anforderung für ein Co-Produkt erstellen

1. Gehen Sie zu **Vertrieb und Marketing \> Arbeitsbereiche \> Verkaufsauftragsverarbeitung und Abfrage**.
1. Wählen Sie **Neu** aus.
1. **Auftrag** auswählen.
1. Geben Sie im Feld **Kundenkonto** einen Wert ein.
    * Beispiel: US-001  
1. Wählen Sie **OK**.
1. Geben Sie im Feld **Artikelnummer** einen Wert ein.
    * Beispiel: P6003  
1. Geben Sie im Feld **Menge** eine Zahl ein.
    * Beispiel: 50000  
1. Wählen Sie **Speichern** aus.

## <a name="create-a-material-plan-for-co-products"></a>Materialplan für Co-Produkte erstellen

1. Schließen Sie die Seite.
1. Schließen Sie die Seite.
1. Wählen Sie **Produktprogrammplanung**.
1. Wählen Sie im Feld **Plan** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
    * Beispiel: MasterPlan  
1. Wählen Sie **Ausführen** aus.
1. Erweitern oder klappen Sie den Abschnitt **Datensätze zum Einschließen** aus.
1. Wählen Sie **Filter** aus.
1. Wählen Sie in der Liste die Zeile für **Feld** = *Elementnummer*.
1. Geben Sie im Feld **Kriterien** einen Wert ein.
    * Beispiel: P6003  
1. Wählen Sie **OK**.
1. Wählen Sie **OK**.
1. Wählen Sie **Bestellvorschläge** aus.
1. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Beispiel: Filtern Sie auf das Feld **Elementnummer** mit einem Wert von 'P6000'.
    * Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.  
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.  
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Erweitern Sie den Abschnitt **Bedarfverursacher**.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
    * Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.  
1. Schließen Sie die Seite.

## <a name="create-a-second-requirement-for-a-co-product"></a>Erstellen Sie eine zweite Anforderung für ein Kuppelprodukt

1. Gehen Sie zu **Vertrieb und Marketing \> Arbeitsbereiche \> Verkaufsauftragsverarbeitung und Abfrage**.
1. Wählen Sie **Neu** aus.
1. **Auftrag** auswählen.
1. Geben Sie im Feld **Kundenkonto** einen Wert ein.
    * Beispiel: US-001  
1. Wählen Sie **OK**.
1. Geben Sie im Feld **Artikelnummer** einen Wert ein.
    * Beispiel: P6003  
1. Geben Sie im Feld **Menge** eine Zahl ein.
    * Beispiel: 50000  
1. Wählen Sie **Speichern** aus.

## <a name="create-a-second-material-plan-for-co-products"></a>Erstellen Sie einen zweiten Materialplan für Kuppelprodukte

1. Wählen Sie im Feld **Plan** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
2. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
    * Beispiel: MasterPlan  
3. Wählen Sie **Ausführen** aus.
4. Erweitern oder klappen Sie den Abschnitt **Datensätze zum Einschließen** aus.
5. Wählen Sie **Filter** aus.
6. Wählen Sie in der Liste die Zeile für **Feld** = *Elementnummer*.
7. Geben Sie im Feld *Kriterien* einen Wert ein.
    * Beispiel: P6003  
8. Wählen Sie **OK**.
9. Wählen Sie **OK**.
10. Wählen Sie **Bestellvorschläge** aus.
11. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Beispiel: Filtern Sie auf das Feld **Elementnummer** mit einem Wert von 'P6000'.
    * Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.  
12. Markieren Sie in der Liste die ausgewählte Zeile.
    * Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.  
13. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
14. Erweitern oder reduzieren Sie den Abschnitt **Bedarfsverursacher**.
15. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
    * Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.  
16. Schließen Sie die Seite.
17. Wählen Sie **Produktprogrammplanung**.
18. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Produktprogrammplanparameter**.
19. Wählen Sie *Nein* im Feld **Alle Planungsprozesse deaktivieren**.
20. Schließen Sie die Seite.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]