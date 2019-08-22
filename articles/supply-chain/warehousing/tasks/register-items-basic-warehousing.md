---
title: Erfassen von Artikeln für einen grundlegendes Warehousing aktivierten Artikel mithilfe eines Artikels eine Wareneingangserfassung
description: Dieses Verfahren zeigt Ihnen an, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie grundlegendes Warehousing im Inventurverwaltungsmodul verwenden.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e64a6df41e43c1b97243a6f7291393982575636
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847230"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Erfassen von Artikeln für einen grundlegendes Warehousing aktivierten Artikel mithilfe eines Artikels eine Wareneingangserfassung

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen an, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie grundlegendes Warehousing im Inventurverwaltungsmodul verwenden. Dies wird in der Regel von einem Sachbearbeiter für Zugänge ausgeführt. Sie können diese Prozedur im Demodatenunternehmen USMF mit den Beispielswerten ausführen, die angezeigt werden.  Wenn Sie nicht USMF verwenden, müssen Sie eine bestätigte Bestellung mit einer offenen Bestellposition haben, bevor Sie dieses Handbuch starten. Der Artikel für die Position muss gelagert sein. Der Artikel muss außerdem einer Lagerdimensionsgruppe zugeordnet werden, in der Standort und Lagerort aktiv sind.


## <a name="create-item-arrival-journal-header"></a>Wareneingangserfassungs-Kopfzeile erstellen
1. Wechseln Sie zu "Lagerverwaltung" > "Journaleinträge" > "Wareneingang" > "Wareneingang".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
    * Wenn Sie USMF verwenden, können Sie WHS eingeben. Wenn Sie andere Daten verwenden, muss die Erfassung, deren Namen Sie auswählen, die folgenden Eigenschaften haben: "Entnahmeort prüfen" muss auf "Kein" festgelegt werden, und "Quarantäneverwaltung" muss auf "Nein" festgelegt werden.  
4. Geben Sie im Feld "Lieferschein" einen Wert ein.
    * Dies ist die Lieferscheinkennung des Lieferscheins, der vom Kreditor ausgestellt wurde. Eindeutige Nummer hinzufügen  
5. Wählen Sie im Feld "Nummer" die Bestellung aus.
6. Klicken Sie auf "OK".

## <a name="add-lines-to-item-arrival-journal"></a>Positionen zur Wareneingangserfassung hinzufügen
1. Klicken Sie auf Funktionen.
2. Klicken Sie auf "Positionen erstellen".
    * Die Positionen können in diese Erfassung manuell eingegeben oder automatisch erstellt werden. Dies zeigt Ihnen an, wie dies automatisch erstellt wird.  
3. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Menge initialisieren".
    * Dies initialisiert die Menge in den Erfassungspositionen mit der Menge, die nicht aus der Bestellposition erfasst wird.  
4. Klicken Sie auf "OK".

## <a name="post-the-journal"></a>Erfassung buchen
1. Klicken Sie auf "Buchen".
2. Klicken Sie auf "OK".

## <a name="generate-the-product-receipt"></a>Produktzugang generieren
1. Klicken Sie auf Funktionen.
2. Klicken Sie auf "Produktzugang".
3. Klicken Sie auf "OK".

