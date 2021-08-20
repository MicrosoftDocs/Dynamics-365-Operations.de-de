---
title: Erstellen einer Bestellung auf Grundlage eines Auftrags
description: Diese Prozedur zeigt, wie Sie eine Bestellung erstellen, die auf einem Auftrag basiert.
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00bd0677113f0029732023dd84fcb1b9bf58648d5611000a3d95376c7d9131e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781829"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Erstellen einer Bestellung auf Grundlage eines Auftrags

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie Sie eine Bestellung erstellen, die auf einem Auftrag basiert. Die Mengen des Produkts in der Bestellung werden dann entsprechend festgelegt, um den Bedarf des ursprünglichen Auftrags zu erfüllen. Zufriedenstellende Verkäufe verlangen, dass diese Methode eine Alternative für eine umfassendere und optimierte Methode der Vertriebsbedarfsplanung ist. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Erstellen einer Bestellung auf Grundlage eines Auftrags
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Aufträge > Alle Aufträge**.
2. Klicken Sie auf **Neu**.
3. Klicken Sie im Feld **Debitorenkonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie auf **OK**.
6. Klicken Sie im Feld **Artikelnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wenn Sie USMF verwenden, können Sie D0001 auswählen.  
8. Geben Sie im Feld **Menge** eine Zahl ein.
9. Klicken Sie auf **Position hinzufügen**.
10. Klicken Sie im Feld **Artikelnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wenn Sie USMF verwenden, können Sie T0020 auswählen.  
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Geben Sie im Feld **Menge** eine Zahl ein.
14. Klicken Sie auf **Speichern**.
15. Klicken Sie im **Aktivitätsbereich** auf **Auftrag**.
16. Klicken Sie auf **Bestellung**. Die Seite **Bestellung erstellen** zeigt alle offenen Auftragspositionen an, die vom Auftrag kopiert wurden. Sie können die Auftragsdetails prüfen und, falls erforderlich, zudem Details wie die Bestellmenge und Preisgestaltungsbedingungen modifizieren, bevor Sie die Einkäufe erstellen. 
17. Wählen Sie die Option **Alle übernehmen** aus.
    - Wenn Sie Direktlieferungen für nur eine Teilmenge der Auftragspositionen generieren möchten, wählen Sie diese einzeln aus.  
    - Das Feld **Kreditorenkonto** ist bereits möglicherweise mit einer Kreditorennummer ausgefüllt. Wenn der Standardkreditor für das Produkt (in der zugehörigen Artikeldeckung) eingerichtet ist, wird dieser Kreditor in die entsprechende Position kopiert. Andernfalls muss ein Kreditor manuell eingegeben werden.  In diesem Leitfaden, unabhängig davon, ob das Feld **Kreditorenkonto** bereits einen Wert oder nicht enthält, weisen die folgenden Schritte Sie an, einen neuen Kreditor auszuwählen, der für jede Position unterschiedlich sein muss.  
18. Klicken Sie im Feld **Kreditorenkonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
19. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
20. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
21. Wählen Sie die zweite Auftragsposition aus.
22. Klicken Sie im Feld **Kreditorenkonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
23. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
24. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
25. Klicken Sie auf **Überprüfen**.
26. Klicken Sie auf **OK**. Die Nachricht informiert Sie darüber, dass eine oder mehrere Bestellungen nun erstellt wurden. Das System legt eine separate Bestellung für jeden Kreditoren an, den Sie für die ausgewählten Auftragspositionen angegeben haben. Das bedeutet, dass, wenn mehrere Auftragspositionen von dem selben Kreditor geliefert werden sollen, eine einzige Bestellung mit mehreren Positionen generiert wird.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Überprüfen Sie die Bestellungen, die aus den Aufträgen erstellt wurden.
1. Klicken Sie im **Aktivitätsbereich** auf **Allgemein**.
2. Klicken Sie auf **Zugeordnete Aufträge**. Die Seite **Zugeordnete Aufträge** führt alle Aufträge auf, die aus dem Auftrag erstellt wurden. In diesem Beispiel gibt es zwei Bestellungen, die für zwei verschiedene Kreditoren generiert werden. 
3. Klicken Sie, um dem Link im Feld **Bestellung** zu folgen. Jede Bestellposition wird der Auftragsposition zugeordnet, die zum betreffenden Einkauf geführt hat. Die Beziehung zu dem Auftrag wird auf der Registerkarte **Produkt** im Inforegister **Positionsdetails**, im **Referenztyp**, der **Referenznummer** und den Feldern **Los-Referenz** angegeben.  
4. Erweitern oder reduzieren Sie den Abschnitt **Positionsdetails**.
5. Klicken Sie auf die Registerkarte **Produkt**.
    - Die **Los-Referenz** gewährleistet, dass die Kosten des aktuellen Einkaufs dem Auftrag zugeordnet werden.  
    - Sie können zu dem ursprünglichen Auftrag navigieren, indem Sie den Link im Feld **Referenznummer** öffnen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]