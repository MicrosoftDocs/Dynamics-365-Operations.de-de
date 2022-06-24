---
title: Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen
description: Dieser Artikel führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 740857e6a902e21588855eef5e36cac68e560898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873277"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen

[!include [banner](../includes/banner.md)]

Dieser Artikel führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop. Es gibt auch Batchaufträge, die für die gleichen Aufgaben konfiguriert werden können. Die Schritte zum Konfigurieren und Ausführen der Batchaufträge werden in anderen Artikeln behandelt. Um diese Prozedur abzuschließen, müssen Buchungen in POS abgeschlossen und dann in Dynamics 365 Commerce einbezogen worden sein. Für diese Aufzeichnung wird das Demo-Datenunternehmen USRT verwendet.

1. Wählen Sie **Shopfinanzdaten** auf der Startseite aus.
2. Wählen Sie **Neuer Auszug** aus.
3. Wählen Sie im Feld **Shopnummer** eine Option in der Dropdownliste aus.
4. Wählen Sie **OK**.
5. Die **Einstellungs** gruppe hat die Einstellungen, mit denen gesteuert wird, welche Buchungen im Auszug enthalten sind und wie sie in Auszugspositionen gruppiert werden. Sie können die **Einstellungs** gruppe öffnen und diese Einstellungen ändern, oder Sie können die Standardwerte verwenden.  
    - Das Feld **Auszugsmethode** definiert, wie die Auszugspositionen gruppiert werden.  
    - Wählen Sie im Feld **Personal/Register** einen Mitarbeiter oder ein Register aus, wenn Sie einen Auszug nur für den bestimmten Mitarbeiter oder das bestimmte Register berechnen möchten.  
6. Wählen Sie im Feld **Abschlussmethode** eine Option aus.
7. Wählen Sie im Aktivitätsbereich **Auszug berechnen** aus.
8. Wählen Sie **Ja** aus.
    - Nachdem der Auszug berechnet wurde, sollte es Positionen geben, die mit Gesamtbeträgen für jede verwendete Zahlungsmethode und Auszugsmethode erstellt wurden.  
    - Geben Sie einen gezählten Betrag in jeder Position ein, wenn er eingegeben oder aktualisiert werden muss. Das gezählte Feld wird mit Beträgen von den Kassenstürzen aufgefüllt, die in POS geleistet werden.  
9. Wählen Sie im Aktivitätsbereich **Auszug buchen** aus.
10. Wählen Sie **Schließen** aus.
11. Schließen Sie den Bereich.
12. Wählen Sie auf der Startseite **Shopfinanzdaten**.
13. Wählen Sie die Registerkarte **Gebuchte Auszüge** aus.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]