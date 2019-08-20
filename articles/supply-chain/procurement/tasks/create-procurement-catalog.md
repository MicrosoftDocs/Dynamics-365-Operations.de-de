---
title: Beschaffungskatalog erstellen
description: In diesem Thema wird erläutert, wie Sie einen Beschaffungskatalog erstellen.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836384"
---
# <a name="create-a-procurement-catalog"></a>Beschaffungskatalog erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Sie einen Beschaffungskatalog erstellen. Diese Aufgabe wird normalerweise von einem Prokuristen ausgeführt. Sie erfahren auch, wie Mitarbeiter den Katalog verwenden können, wenn sie eine Anforderung erstellen. Bevor Sie einen Katalog erstellen können, muss es in Ihrem System eine Beschaffungskategoriehierarchie geben. Die Hierarchie wird vom neuen Katalog zusammen mit allen Produkten geerbt, die sich in der Hierarchie befinden. Sie können diesen Leitfaden im Demodatenunternehmen USMF verwenden, in dem die Beschaffungskategoriehierarchie verfügbar ist, sowie die Beispiele, die in den Prozedurschritten verwendet werden.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Sicherstellen, dass eine Beschaffungskategoriehierarchie vorhanden ist
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Beschaffungskategorien**. Eine Beschaffungskategoriehierarchie ist im USMF-Demodatenunternehmen verfügbar, und Produkte sind der Kategorie **Bürogeräte/Computer** hinzugefügt worden. Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie den Leitfaden entsperren, wenn Sie die Kategorie durchsuchen möchten. Wenn eine Hierarchie nicht verfügbar wäre, würden Sie sie erstellen, indem Sie auf **Neu** klicken. Dies kann nur einmal ausgeführt werden.  
2. Schließen Sie die Seite.

## <a name="create-a-catalog"></a>Einen Katalog erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kataloge > Beschaffungskataloge**.
2. Klicken Sie auf **Neuer Beschaffungskatalog**, um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld **Name** einen Wert ein.
4. Wählen Sie **OK**.
5. Erweitern Sie im Baum **UNTERNEHMENSBESCHAFFUNGSKATEGORIEN**.
6. Erweitern Sie im Baum **BÜROGERÄTE**.
7. Wählen Sie im Baum **Computer** aus.

  - Die Produkte aus der Beschaffungskategorie werden in der Liste angezeigt. Wenn Sie ein Produkt der Kategorie hinzufügen möchten, müssen Sie dies auf der Seite **Beschaffungskategoriehierarchie** oder auf der Seite **Artikeldetails** erledigen.  
  - Der **standardmäßige** Aktualisierungstyp bestimmt, ob neue Produkte, die der Beschaffungskategoriehierarchie hinzugefügt wurden, im Katalog sofort sichtbar sind. Wenn der Aktualisierungstyp auf **Dynamisch** festgelegt ist, sind Änderungen sofort sichtbar. Wenn der Aktualisierungstyp auf **Statisch** festgelegt ist, sind neue Produkte nur sichtbar, wenn Personen den Katalog benutzen, nachdem der Katalog erneut veröffentlicht wurde. Die Aktivität **Veröffentlichen** ist im Aktivitätsbereich oben auf der Seite verfügbar. Wenn Produkte von der Beschaffungskategoriehierarchie entfernt werden, ist die Änderung sofort sichtbar, unabhängig vom Wert im Feld **Standardmäßiger Aktualisierungstyp**.  

8. Wählen Sie im Aktivitätsbereich **Kategorienavigation** aus, und stellen Sie sicher, dass **Aktivieren** ausgewählt ist.
9. Wählen Sie **Katalog aktivieren**.
10. Schließen Sie die Seite.

## <a name="make-the-catalog-visible"></a>Den Katalog sichtbar machen
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Einstellungen > Richtlinien > Einkaufsrichtlinien**.
2. Wählen Sie die **Beschaffungsrichtlinie USMF** aus. Sie müssen die Einkaufsrichtlinie für die juristische Person auswählen, in der die Arbeitskraft, der mit Ihrem Benutzerprofil verbunden ist, Produkte bestellen darf. In den USMF-Demodaten ist der Benutzer „Administrator“ mit der Arbeitskraft **Julia Funderburk** verbunden, und sie bestellt standardmäßig Produkte in USMF.  
3. Wählen Sie den Katalog aus, das Sie soeben erstellt haben.
4. Wählen Sie **OK**.

## <a name="use-the-catalog"></a>Den Katalog verwenden
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Bestellanforderungen > Alle Bestellanforderungen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Wert ein.
4. Wählen Sie **OK**.
5. Wählen Sie **Produkte hinzufügen** aus.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Sie können die Kategoriehierarchie auf der linken Seite oder den Filter oben an der Liste verwenden, um die Produkte zu filtern.  
7. Wählen Sie **Zu Positionen hinzufügen**.
8. Wählen Sie **OK**.

