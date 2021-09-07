---
title: Anlagen von "Kreditoren" erstellen und anschaffen
description: Diese Prozedur führt Sie durch die Erstellung und den Erwerb einer Anlage mit dem Kaufprozess.
author: saraschi2
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbac069362a15b5ab1d2dbf88a732a14a3cf709d
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394657"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Anlagen von "Kreditoren" erstellen und anschaffen

[!include [banner](../../includes/banner.md)]

Diese Prozedur führt Sie durch die Erstellung und den Erwerb einer Anlage mit dem Kaufprozess.  Dabei werden der "Buchhalter" und die "Sachbearbeiter Kreditorenkonten" und das Demo-Unternehmen USMF verwendet.


## <a name="set-fixed-assets-parameters"></a>Anlagenparametern festlegen
1. Wechseln Sie im **Navigationsbereich** zu **Module > Anlagen > Einstellungen > Anlagenparameter**.
2. Erweitern Sie das Inforegister **Bestellungen**.
3. Aktivieren Sie das Kontrollkästchen **Anlagenanschaffung aus Einkauf zulassen**.
4. Aktivieren Sie das Kontrollkästchen **Anlage bei Buchung von Produktzugang oder Rechnung erstellen**.

## <a name="create-a-new-vendor-invoice"></a>Eine neue Kreditorenrechnung erstellen
1. Wechseln Sie im **Navigationsbereich** zu **Module > Kreditoren > Arbeitsbereiche > Kreditorenrechnungseintrag**.
2. Klicken Sie auf **Neue Kreditorenrechnung**.
3. Klicken Sie im Feld **Rechnungskonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld **Zahl** einen Wert ein.
6. Geben Sie im Feld **Buchungsdatum** ein Datum ein.
7. Klicken Sie auf **Position hinzufügen**.
8. Klicken Sie im Feld **Artikelnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen. Entweder nicht gelagerte Artikel oder Beschaffungskategorien können für Anlagenanschaffung verwendet werden.  
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Geben Sie im Feld **Menge** eine Zahl ein. Eine Rechnungsposition erstellt nur eine Anlage, unabhängig von Menge. Der Rechnungsmengen-Feldwert wird zur Anlagenmenge übertragen.  
11. Geben Sie im Feld **Einzelpreis** eine Zahl ein.
12. Erweitern Sie das Inforegister **Positionsdetails**.
13. Klicken Sie auf die Registerkarte **Anlagen**.
14. Aktivieren Sie das Kontrollkästchen **Neue Anlage erstellen**.
15. Klicken Sie im Feld **Anlagengruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
16. Wählen Sie in der Liste die Anlagengruppe aus, die beim Erstellen der neuen Anlage zu verwenden ist.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Klicken Sie auf **Buchen**. Die Anlage wird erstellt und abgerufen, wann die Rechnung gebucht wird.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
