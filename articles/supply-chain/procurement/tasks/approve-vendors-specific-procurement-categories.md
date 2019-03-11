---
title: Kreditoren für spezifische Beschaffungskategorien genehmigen
description: Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308390"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Kreditoren für spezifische Beschaffungskategorien genehmigen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind. Diese Prozedur zeigt Ihnen, wie man angibt, dass ein Kreditor für eine spezifische Beschaffungskategorie genehmigt oder bevorzugt ist. Diese Aufgabe ist in der Regel von einem Beschaffungsspezialisten ausgeführt. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.

1. Klicken Sie auf "Beschaffung" > "Kreditoren" > "Alle Kreditoren".
2. Wählen Sie den Kreditor aus, den Sie als genehmigten oder bevorzugten Kreditor für eine Kategorie festgelegt haben möchten.
3. Klicken Sie im Aktivitätsbereich auf "Allgemein".
4. Klicken Sie auf "Kategorien".
5. Klicken Sie auf "Kategorie hinzufügen".
6. Wählen Sie im Feld "Kategorie" die Option "BÜRO- UND SCHREIBTISCHZUBEHÖR (BÜRO- UND SCHREIBTISCHZUBEHÖR) aus.
7. Wählen Sie im Feld "Kreditorkategoriestatus" die Option "Bevorzugt" aus.
    * Es ist möglich, mehr als einen bevorzugten Kreditor für eine Kategorie anzugeben.  
8. Klicken Sie auf "Speichern".
9. Wechseln Sie zu "Beschaffung" > "Beschaffungskategorien".
10. Wählen Sie im Baum die Option "UNTERNEHMENSBESCHAFFUNGSKATEGORIEN\BÜRO- UND SCHREIBTISCHZUBEHÖR" aus.
11. Erweitern Sie den Abschnitt "Kreditoren".
    * Überprüfen Sie, ob der Kreditor, den Sie ausgewählt haben, als bevorzugter Kreditor für die Kategorie "Büro- und Schreibtischzubehör" angezeigt wird. Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie möglicherweise auf die Schaltfläche "Entsperren" klicken, um einen Bildlauf nach unten zur Kreditorenliste durchführen zu können.  Es ist auch möglich, bevorzugte und genehmigte Kreditoren auf dieser Seite hinzuzufügen.  
12. Erweitern Sie im Baum die Option "BÜRO- UND SCHREIBTISCHZUBEHÖR".
13. Wählen Sie im Baum "Scheren" aus.
14. Wählen Sie "Nein" im Feld "Kreditoren aus übergeordneter Kategorie erben:" aus.
15. Wählen Sie "Ja" im Feld "Kreditoren aus übergeordneter Kategorie erben:" aus.

