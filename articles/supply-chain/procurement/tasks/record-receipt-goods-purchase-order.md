--- 
title: Den Warenzugang auf der Bestellung erfassen
description: Diese Prozedur zeigt Ihnen an, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird.
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Den Warenzugang auf der Bestellung erfassen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen an, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird. Es ist auch möglich, den Produktzugang im Lagerort zu erfassen und ihn dann später auf der Bestellung aufzuzeichnen. Diese Aufgabe wird gewöhnlich von einem Einkäufer oder einem Kreditorenkontenkoordinator ausgeführt. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Das Beispiel umfasst Schritte, um eine einfache Bestellung zu erstellen, damit Sie die Prozedur als Aufgabenleitfaden wiedergeben können. Wenn Sie die Prozedur mit Ihren eigenen Daten verwendeten, würden Sie bei der Unteraufgabe "Warenzugang erfassen" beginnen.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Eine neue Bestellung für den Warenzugang vorbereiten
1. Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Kreditorenkonto" den Wert US-101 ein.
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" den Wert M0001 ein.
6. Geben Sie im Feld "Menge" den Wert "5" ein.
7. Klicken Sie im Aktivitätsbereich auf "Einkauf".
8. Klicken Sie auf "Bestätigen".

## <a name="record-receipt-of-goods"></a>Warenzugang erfassen
1. Klicken Sie im Aktivitätsbereich auf "Empfangen".
2. Klicken Sie auf "Produktzugang".
    * Das Feld "Menge" ermöglicht es Ihnen, verschiedene Optionen für die Menge auszuwählen, die Sie empfangen möchten. Zum Beispiel wenn eine Menge vorher im Lagerort registriert worden ist, können Sie "Erfasste Menge" auswählen.  Für dieses Beispiel verwenden Sie den Wert "Bestellte Menge".   
3. Geben Sie im Feld "Produktzugang" irgendeinen Wert ein.
    * Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.  
4. Erweitern Sie den Abschnitt "Positionen".
5. Legen Sie die Menge auf "4" fest.
    * Hier sind Sie in der Lage, die Menge manuell zu anzugeben, die für jede Position zum Auftrag empfangen wird.  
6. Reduzieren Sie den Abschnitt "Positionen".
7. Klicken Sie auf "OK".
    * Die Waren sind jetzt auf der Bestellung als empfangen erfasst worden und eine Produktzugangserfassung ist als Dokument, um dies widerzuspiegeln, erstellt worden. Sie können die Aktivität "Produktzugang" verwenden, um die Erfassungen zu überprüfen, die mit der Bestellung erstellt wurden und um zu sehen, was wann empfangen wurde.  


