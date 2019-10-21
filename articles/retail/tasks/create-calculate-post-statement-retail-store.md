---
title: Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen
description: Dieses Thema führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.
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
ms.openlocfilehash: 4517b9ddeb648b3d789773fc0dcb1ecd3c8be85c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024797"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen

[!include[task guide banner](../includes/task-guide-banner.md)]

Dieses Thema führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop. Es gibt auch Batchaufträge, die für die gleichen Aufgaben konfiguriert werden können. Die Schritte zum Konfigurieren und Ausführen der Batchaufträge werden in anderen Themen behandelt. Um diese Prozedur abzuschließen, müssen Buchungen in POS abgeschlossen und dann in Dynamics 365 Retail einbezogen worden sein. Für diese Aufzeichnung wird das Demo-Datenunternehmen USRT verwendet.

1. Wählen Sie **Finanzdaten für den Einzelhandelsshop** auf der Startseite aus.
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
12. Wählen Sie **Finanzdaten für den Einzelhandelsshop** auf der Startseite aus.
13. Wählen Sie die Registerkarte **Gebuchte Auszüge** aus.

