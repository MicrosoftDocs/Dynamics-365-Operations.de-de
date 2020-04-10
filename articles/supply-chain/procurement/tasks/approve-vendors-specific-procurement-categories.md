---
title: Kreditoren für spezifische Beschaffungskategorien genehmigen
description: In diesem Thema wird erläutert, wie Kreditoren für bestimmte Beschaffungskategorien in Dynamics 365 Supply Chain Management genehmigt werden.
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
ms.openlocfilehash: 135b3a6bea2c0a8940550299504139551c9c3559
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147502"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Kreditoren für spezifische Beschaffungskategorien genehmigen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Kreditoren für bestimmte Beschaffungskategorien in Dynamics 365 Supply Chain Management genehmigt werden. Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind. Diese Prozedur zeigt Ihnen, wie man angibt, dass ein Kreditor für eine spezifische Beschaffungskategorie genehmigt oder bevorzugt ist. Diese Aufgabe ist in der Regel von einem Beschaffungsspezialisten ausgeführt. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.

1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Kreditoren > Alle Kreditoren**.
2. Wählen Sie den Kreditor aus, den Sie als genehmigten oder bevorzugten Kreditor für eine Kategorie festgelegt haben möchten.
3. Wählen Sie im Aktivitätsbereich **Allgemein** aus.
4. Wählen Sie **Kategorien**.
5. Wählen Sie **Kategorie hinzufügen**.
6. Wählen Sie im Feld **Kategorie** die Option **BÜRO- UND SCHREIBTISCHZUBEHÖR (BÜRO- UND SCHREIBTISCHZUBEHÖR)** aus.
7. Wählen Sie im Feld **Kreditorkategoriestatus** die Option **Bevorzugt** aus. Es ist auch möglich, mehr als einen bevorzugten Kreditor für eine Kategorie anzugeben.  
8. Wählen Sie **Speichern**.
9. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Beschaffungskategorien**.
10. Wählen Sie im Baum die Option **UNTERNEHMENSBESCHAFFUNGSKATEGORIEN\BÜRO- UND SCHREIBTISCHZUBEHÖR** aus.
11. Erweitern Sie den Abschnitt **Kreditoren**. Überprüfen Sie, ob der Kreditor, den Sie ausgewählt haben, als bevorzugter Kreditor für die Kategorie "Büro- und Schreibtischzubehör" angezeigt wird. Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie möglicherweise die Schaltfläche **Entsperren** wählen, um einen Bildlauf nach unten zur Kreditorenliste durchführen zu können.  Es ist aber auch möglich, bevorzugte und genehmigte Kreditoren auf dieser Seite hinzuzufügen.  
12. In der Struktur erweitern Sie den Knoten **BÜRO- UND SCHREIBTISCHZUBEHÖR** und wählen Sie **Scheren** aus.
13. Wählen Sie **Nein** im Feld **Kreditoren aus übergeordneter Kategorie erben:** aus.
14. Wählen Sie **Ja** im Feld **Kreditoren aus übergeordneter Kategorie erben:** aus.

