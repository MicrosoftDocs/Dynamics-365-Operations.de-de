---
title: Vertriebsprovisionsregeln einrichten
description: Dieses Verfahren zeigt Ihnen, wie Vertriebsprovisionsberechnung und die Nachverfolgung aktivieren.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4507405039cd27a071e0f0ed8bfad31fd30f16f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203203"
---
# <a name="set-up-sales-commission-rules"></a>Vertriebsprovisionsregeln einrichten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen, wie Vertriebsprovisionsberechnung und die Nachverfolgung aktivieren. Die Prozedur zeig, wie Debitoren- und Artikelprovisionsgruppen erstellt werden und ein ausgewählter Debitor und ein Produkt zu den jeweiligen Gruppen verknüpft werden. Diese Gruppen werden im Formular "Provisionsberechnungseinstellung" verwendet, um einen Debitor, einen Artikel und eine Verkäuferkombination zu erstellen, die mit dem Auftrag übereinstimmen muss, um die Verkäufer für eine Provision zu berechtigen. Debitoren- und Artikelprovisionsgruppen zu erstellen ist optional, da die Berechnung der Provision auch für einen einzelnen Debitor und/oder einen Artikel ausgeführt werden kann. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.


## <a name="set-up-commission-groups-and-commission-rates"></a>Einrichten von Provisionsgruppen und Provisionssätzen
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Provisionen > Debitorengruppen für Provision**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Gruppe** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie **Speichern**.
6. Schließen Sie die Seite.
7. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Provisionen > Artikelgruppen**.
8. Wählen Sie **Neu** aus.
9. Geben Sie im Feld **Gruppe** einen Wert ein.
10. Geben Sie im Feld **Name** einen Wert ein.
11. Wählen Sie **Speichern**.
12. Schließen Sie die Seite.
13. Wechseln Sie zu **Vertrieb und Marketing > Provisionen > Vertriebsgruppen**.
    - Eine Provisionsverkaufsgruppe gibt die Mitarbeiter mit den Verkäuferrollen an, die berechtigt sind, eine Provision zu erhalten, wenn ein bestimmte Artikel zugewiesener Verkäufer der relevanten Verkaufsgruppen Artikel kauf.  
    - Im USMF-Demodatunternehmen gibt eine Verkaufsgruppe mit dem Namen "Vertriebsmitarbeiter US".  
14. Wählen Sie im **Aktivitätsbereich** **Allgemein** aus.
15. Klicken Sie auf **Verkäufer**. Die Seite "Vertriebsmitarbeiter" zeigt eine Liste der Vertriebsmitarbeiter des Unternehmens, die einer bestimmten Provisionsgruppe zugeordnet sind. Sie können mehrere Verkäufer derselben Gruppe zuweisen und den jeweilige Anteil der gesamten Kommissionsgebühr als prozentualen Wert definieren. Die gesamten Provisionsanteile zu allen Mitarbeitern dürfen 100 nicht überschreiten. 
16. Markieren Sie in der Liste die ausgewählte Zeile.
17. Wählen Sie **Bearbeiten** aus.
18. Legen Sie **Provisionsanteil** auf „50“ fest.
19. Klicken Sie auf **Neu**.
20. Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
21. Verwenden Sie den **Schnellfilter**, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld Name mit einem Wert "Susan Burk".
22. Klicken Sie auf **Auswählen**.
23. Legen Sie **Provisionsanteil** auf „50“ fest.
24. Klicken Sie auf **Speichern**.
25. Wechseln Sie zu **Vertrieb und Marketing > Provisionen > Provisionsberechnung**. Auf der Seite **Provisionsberechnung** definieren Sie den Kommissionssatz, den der Mitarbeiter für eine Verkaufsbuchung erhalten soll, wenn diese eine vorab festgelegte Kombination aus Debitor und Produkt enthält. Im Rahmen der Kommissionssatzeinrichtung müssen Sie die Provisionsberechnungsbasis angeben und ob sie Rabatte umfassen oder ausschließen soll. Sie können auch einen Gültigkeitszeitraum für den Kommissionssatz eingeben.  
26. Klicken Sie auf **Neu**.
27. Wählen Sie im Feld **Artikelcode** die Option „Gruppe“ aus.
28. Klicken Sie im Feld **Artikelrelation** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
29. Wählen Sie in der Liste die Gruppe aus, die Sie erstellt haben.
30. Wählen Sie im Feld **Debitorcode** „Gruppe“ aus.
31. Klicken Sie im Feld **Debitorenrelation** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
32. Wählen Sie in der Liste die Gruppe aus, die Sie erstellt haben.
33. Klicken Sie im Feld **Vertriebsmitarbeiter** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
34. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    - Verwenden Sie die Option "Vor Positionsrabatt".  
    - Verwenden Sie die Option "Umsatzerlös" als Grundlage für Provisionswertsberechnung.    
35. Geben Sie im Feld "Provisionsprozentsatz" eine Zahl ein.
36. Klicken Sie auf **Speichern**.

## <a name="setting-up-commission-posting"></a>Einrichten der Provisionsbuchung
1. Wechseln Sie zu **Navigationsbereich > Vertrieb und Marketing > Provisionen > Provisionsbuchung**. Kommissionsgebühren werden den Mitarbeitern ausgezahlt und müssen daher eingerichtet werden, um richtige wertmäßige Buchung auf die entsprechenden Konten im **Hauptbuch** sicherzustellen. Dieser wird auf der Seite **Provisionsbuchung** durchgeführt. Überprüfen Sie die Einrichtung im aktuellen Unternehmen. In der Regel werden Provisionsbeträge in ein dediziertes Ausgabenkonto gebucht über ein dediziertes Kreditorenkonto ausgeglichen. Wenn Sie nicht die Provisionsbuchungsregeleinstellung durchgeführt haben, kann das System Rechnungsstellung eines Auftrags der nicht freigegebene Provisionen hat nicht durchführen.  
2. Schließen Sie die Seite.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Zuweisen einer Provisionsgruppe zu einem Debitor und einem Produkt
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Debitoren > Alle Debitoren**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf **Bearbeiten**.
5. Erweitern Sie den **Auftragsstandardabschnitt**.
6. Klicken Sie im Feld **Provisionsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Wählen Sie in der Liste die Gruppe aus, die Sie erstellt haben.
8. Klicken Sie im Feld **Verkaufsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie auf **Speichern**.
11. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
12. Verwenden Sie den **Filter**, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "T0020".
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Klicken Sie auf **Bearbeiten**.
15. Erweitern Sie den Abschnitt **Verkaufen**.
16. Klicken Sie im Feld **Provisionsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
17. Wählen Sie in der Liste die Provisionsgruppe aus, die Sie erstellt haben.
18. Wählen Sie **Speichern**.

