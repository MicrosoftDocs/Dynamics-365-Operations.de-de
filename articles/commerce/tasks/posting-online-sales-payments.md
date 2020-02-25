---
title: Buchen von Online-Verkäufen und -Zahlungen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf7f72be22539271649aa7f5541735b3d24dab66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022634"
---
# <a name="posting-of-online-sales-and-payments"></a>Buchen von Online-Verkäufen und -Zahlungen

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.

Die Buchung von Online-Verkäufen und Zahlungen ist ein zweistufiger Prozess.

- Abruf der Online-Commerce-Transaktionsdaten in der Zentrale.
- Synchronisieren von Aufträgen, um Kundenaufträge in der Zentrale anzulegen.

Das Abrufen der Online-Transaktionsdaten kann entweder durch manuelles Ausführen des P-Jobs oder durch Erstellen eines wiederkehrenden Batch-Jobs erfolgen.

### <a name="manually-running-the-p-job"></a>Manuelles Ausführen des P-Jobs

1. Navigieren Sie zu alle Arbeitsbereiche > Einzelhandel und Commerce IT.
2. Klicken Sie auf Verteilungsplan.
3. Wählen Sie P-0001.
4. Passen Sie bei Bedarf die Gruppen der Kanaldatenbank an.
5. Klicken Sie auf Jetzt ausführen
6. Klicken Sie auf „Ja“.

### <a name="scheduling-a-recurring-p-job"></a>Einplanen eines wiederkehrenden P-Jobs

1. Navigieren Sie zu alle Arbeitsbereiche > Einzelhandel und Commerce IT.
2. Klicken Sie auf Verteilungsplan.
3. Wählen Sie P-0001.
4. Klicken Sie auf Batch-Job erstellen.
5. Klicken Sie im Hintergrund auf Ausführen.
5. Aktivieren Sie die Stapelverarbeitung.
6. Klicken Sie auf Wiederholung.
7. Wählen Sie die Option "Kein Enddatum" aus.
8. Geben Sie im Feld Zähler das Intervall zwischen den Läufen in Minuten ein. Typischerweise wäre dies 5-10.
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".

Aufträge können entweder durch manuelles Ausführen des Jobs „Aufträge synchronisieren“ oder durch Erstellen eines wiederkehrenden Batch-Jobs synchronisiert werden.

### <a name="manually-running-order-synchronization"></a>Manuell laufende Auftragssynchronisation 

Führen Sie diese Schritte aus, um den Job „Aufträge synchronisieren“ einmal manuell auszuführen.

1. Gehen Sie zu Alle Arbeitsbereiche > Finanzdaten für Shop.
2. Klicken Sie auf "Aufträge synchronisieren".
3. Wählen Sie im Organisationshierarchie-Feld Einzelhandelsgeschäfte nach Region aus.
    * Wählen Sie entweder einen bestimmten Online-Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.  
    * Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.  
4. Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".
5. Stapelverarbeitung deaktivieren
6. Klicken Sie auf "Wiederholung".
7. Wählen Sie die Option Ende nach
8. Geben Sie im Feld Ende nach 1 ein.
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".

### <a name="scheduling-recurring-order-synchronization"></a>Terminierung der Synchronisation wiederkehrender Aufträge

Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Gehen Sie zu Alle Arbeitsbereiche > Finanzdaten für Shop.
2. Klicken Sie auf "Aufträge synchronisieren".
3. Wählen Sie im Organisationshierarchie-Feld Einzelhandelsgeschäfte nach Region aus.
    * Wählen Sie entweder einen bestimmten Online-Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.  
    * Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.  
4. Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".
5. Batch-Verarbeitung aktivieren
6. Klicken Sie auf "Wiederholung".
7. Wählen Sie die Option "Kein Enddatum" aus.
8. Geben Sie im Feld Zähler das Intervall zwischen den Läufen in Minuten ein. Typischerweise wäre dies 2-20.
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".

## <a name="data-entities-involved-in-the-process"></a>Am Prozess beteiligte Dateneinheiten

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
