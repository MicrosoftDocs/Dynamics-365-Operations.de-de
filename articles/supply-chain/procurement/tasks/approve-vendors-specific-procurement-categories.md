---
title: Kreditoren für spezifische Beschaffungskategorien genehmigen
description: In diesem Thema wird erläutert, wie Kreditoren für bestimmte Beschaffungskategorien in Dynamics 365 for Finance and Operations genehmigt werden.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867148"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Kreditoren für spezifische Beschaffungskategorien genehmigen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Kreditoren für bestimmte Beschaffungskategorien in Dynamics 365 for Finance and Operations genehmigt werden. Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind. Diese Prozedur zeigt Ihnen, wie man angibt, dass ein Kreditor für eine spezifische Beschaffungskategorie genehmigt oder bevorzugt ist. Diese Aufgabe ist in der Regel von einem Beschaffungsspezialisten ausgeführt. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.

1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Kreditoren > Alle Kreditoren**.
2. Wählen Sie den Kreditor aus, den Sie als genehmigten oder bevorzugten Kreditor für eine Kategorie festgelegt haben möchten.
3. Wählen Sie im Aktivitätsbereich **Allgemein** aus.
4. Wählen Sie **Kategorien**.
5. Wählen Sie **Kategorie hinzufügen**.
6. Wählen Sie im Feld **Kategorie** die Option **BÜRO- UND SCHREIBTISCHZUBEHÖR (BÜRO- UND SCHREIBTISCHZUBEHÖR)** aus.
7. Wählen Sie im Feld **Kreditorkategoriestatus** die Option **Bevorzugt** aus. Es ist möglich, mehr als einen bevorzugten Kreditor für eine Kategorie anzugeben.  
8. Wählen Sie **Speichern**.
9. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Beschaffungskategorien**.
10. Wählen Sie im Baum die Option **UNTERNEHMENSBESCHAFFUNGSKATEGORIEN\BÜRO- UND SCHREIBTISCHZUBEHÖR** aus.
11. Erweitern Sie den Abschnitt **Kreditoren**. Überprüfen Sie, ob der Kreditor, den Sie ausgewählt haben, als bevorzugter Kreditor für die Kategorie "Büro- und Schreibtischzubehör" angezeigt wird. Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie möglicherweise die Schaltfläche **Entsperren** auswählen, um einen Bildlauf nach unten zur Kreditorenliste durchführen zu können.  Es ist auch möglich, bevorzugte und genehmigte Kreditoren auf dieser Seite hinzuzufügen.  
12. In der Struktur erweitern Sie den Knoten **BÜRO- UND SCHREIBTISCHZUBEHÖR** und wählen Sie **Scheren** aus.
13. Wählen Sie **Nein** im Feld **Kreditoren aus übergeordneter Kategorie erben:** aus.
14. Wählen Sie **Ja** im Feld **Kreditoren aus übergeordneter Kategorie erben:** aus.

