---
title: " Einen Auszug für ein Einzelhandelsgeschäft erstellen, berechnen und buchen"
description: Diese Prozedur führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354390"
---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Einen Auszug für ein Einzelhandelsgeschäft erstellen, berechnen und buchen

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop. Es gibt auch Batchaufträge, die für die gleichen Aufgaben konfiguriert werden können. Die Schritte zum Konfigurieren und Ausführen der Batchaufträge werden in anderen Themen behandelt. Um dieses Verfahren abzuschließen, müssen Transaktionen enthalten sein, die in POS abgeschlossen und dann in Dynamics AX einbezogen wurden. Für diese Aufzeichnung wird das Demo-Datenunternehmen USRT verwendet. Dieses Verfahren bezieht sich möglicherweise auf Microsoft Dynamics AX. Beachten Sie, dass Dynamics AX nun als Microsoft Dynamics 365 for Operations bezeichnet wird.

1. Gehen Sie zu Alle Arbeitsbereiche >.. > Finanzdaten für den Einzelhandelsshop.
2. Klicken Sie auf "Neuer Auszug".
3. Klicken Sie im Feld "Shopnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf "OK".
    * Die Einstellungsgruppe hat die Einstellungen, mit denen gesteuert wird, welche Buchungen im Auszug enthalten sind und wie sie in Auszugspositionen gruppiert werden. Sie können die Einstellungsgruppe öffnen und diese Einstellungen ändern, oder Sie können die Standards verwenden.  
    * Das Auszugsmethodenfeld definiert, wie die Auszugspositionen gruppiert werden.  
    * Wählen Sie einen Mitarbeiter oder ein Register aus, wenn Sie einen Auszug nur für den bestimmten Mitarbeiter oder das bestimmte Register berechnen möchten.  
6. Wählen Sie im Feld "Abschlussmethode" eine Option aus.
7. Klicken Sie auf "Auszug berechnen".
8. Klicken Sie auf "Ja".
    * Nachdem der Auszug berechnet wurde, sollte es Positionen geben, die mit Gesamtbeträgen für jede verwendete Zahlungsmethode und Auszugsmethode erstellt wurden.  
    * Geben Sie einen gezählten Betrag in jeder Position ein, wenn er eingegeben oder aktualisiert werden muss. Das gezählte Feld wird mit Beträgen von den Kassenstürzen aufgefüllt, die in POS geleistet werden.  
9. Klicken Sie auf "Auszug buchen".
10. Klicken Sie auf "Schließen".
11. Navigieren Sie zu Einzelhandel und Handel > Kanäle > Finanzdaten für den Einzelhandelsshop.
12. Klicken Sie auf die Registerkarte "Gebuchte Auszüge".

