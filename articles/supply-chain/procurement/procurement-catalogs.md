---
title: Beschaffungskataloge (Überblick)
description: In diesem Artikel wird zusammenfassend beschrieben, wie Einkäufer Beschaffungskataloge einrichten und verwalten können. Beschaffungskataloge definieren Artikel und Dienstleisungen, die Unternehmensmitarbeiter für den internen Gebrauch bestellen können.
author: mkirknel
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, CatDisplayProductRelationAdd
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64c7c2787e2ac996e3016f5b23fc48582f5533ad
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018904"
---
# <a name="procurement-catalogs-overview"></a>Beschaffungskataloge (Überblick)

[!include [banner](../includes/banner.md)]

In diesem Artikel wird zusammenfassend beschrieben, wie Einkäufer Beschaffungskataloge einrichten und verwalten können. Beschaffungskataloge definieren Artikel und Dienstleisungen, die Unternehmensmitarbeiter für den internen Gebrauch bestellen können.

"Einkäufer"können Kataloge von Artikeln und Dienstleistungen erstellen und verwalten, die für den internen Gebrauch einer Organisation gekauft werden können. Nachdem Kataloge eingerichtet sind, können die Mitarbeiter Bestellanforderungen erstellen, um darüber zu bestellen. Die Kataloge können verwendet werden, um Einkaufsrichtlinien zu erzwingen, damit Mitarbeiter nur die Artikel und Dienstleistungen bestellen können, die für ihre kaufende juristische Person zulässig sind. Beim Erstellen eines Beschaffungskatalogs müssen Sie die folgenden Aufgaben beachten:

-   Konfigurieren Sie Ihre Beschaffungskategoriehierarchie, bevor Sie den Katalog erstellen.
-   Bestimmen, welche Produkte Mitarbeiter bestellen können. Sie können bestimmte Produkte in einem Katalogknoten anzeigen oder ausblenden, oder Sie können alle Produkte aus einem Knoten anzeigen oder ausblenden.
-   Bestimmen, wie viele Beschaffungskataloge erforderlich sind. Der Zugriff auf einen Beschaffungskatalog wird durch die Katalogrichtlinienregel bestimmt, die Sie für die juristische Person und Organisationseinheit konfigurieren, der ein Mitarbeiter zugewiesen ist.

Einige Faktoren bestimmen die Produkte, die Mitarbeiter bestellen können und die Beschaffungskategorien, die sie verwenden können, wenn sie Bestellanforderungen erstellen:

-   Die Richtlinienregel für Kategoriezugriff in der Einkaufsrichtlinie bestimmt, welche Beschaffungskategorien in der Bestellanforderung verfügbar sind. Wenn keine Regel definiert ist, sind alle Beschaffungskategorien verfügbar.
-   Mitarbeiter können ein Produkts nur dann ebstellen, wenn es im aktiven Beschaffungskatalog für Ihre Organisation ist und wenn es in einem aktivierten Knoten und nicht ausgeblendet ist. Das Produkt muss außerdem in einer Kategorie sein, zu der ein bestimmter Mitarbeiter entsprechend der "Richtlinienregel für Kategoriezugriff" Zugriff hat.
-   Die Katalogrichtlinienregel gibt den Katalog an, der verwendet wird. Wenn keine Katalogrichtlinienregel definiert wird, bestimmt die Kategoriezugriffsregel allein die Produkte, die ein Mitarbeiter mit der Anforderung bestellen kann.

## <a name="prerequisites"></a>Erforderliche Komponenten
In der folgenden Tabelle werden die Aufgaben beschrieben, die abgeschlossen sein müssen, bevor ein Einkäufer einen Beschaffungskatalog erstellen kann.

| Aufgabe                                                | Rolle               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Richten Sie eine Beschaffungskategoriehierarchie ein.            | Leiter Einkauf | Beschaffungskategoriehierarchien dienen zum Klassifizieren von Artikeln oder Buchungen für das Finanz- und Rechnungswesen. Durch Verwendung einer Beschaffungskategoriehierarchie können Unternehmen strategisch Kategorien, Produkte, Kreditoren und andere Beschaffungsfaktoren von einem zentralen Ausgangspunkt aus strategisch verwalten. Eine Beschaffungskategoriehierarchie wird für eine gesamte Organisation definiert. Der Katalog basiert auf Grundlage der Beschaffungskategoriehierarchie: die Kategorien in der Hierarchie werden Knoten im Katalog. Die Kreditoren und Produkte sind in Ihrem Katalog enthalten. |
| Fügen Sie Kreditoren und Produkten zu Beschaffungskategorien hinzu. | Leiter Einkauf | Nachdem Sie die Beschaffungskategoriehierarchie für die Organisation erstellt haben, kann jede Beschaffungskategorie bestimmten Kreditoren, Produkten usw. zugeordnet werden. Diese Zuordnungen werden automatisch in den Katalog kopiert.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Einrichten eines Katalogs
Nachdem die Voraussetzungen erfüllt wurden, können Sie Kataloge einrichten. Sie können entweder einen Katalog erstellen, den die gesamte Organisation verwendet oder mehrere Kataloge, die von verschiedenen Abteilungen in der Organisation verwendet werden. Wenn Sie einen Katalog für die gesamte Organisation erstellen, wird der Zugriff auf den Katalog durch Ihre Bestellungsrichtlinien definiert.  

Der Katalog definiert, welche Produkte verfügbar sind, wenn Bestellanforderungen erstellt werden, allerdings können Sie Kategoriezugriffsrichtlinienregeln verwenden, um zusätzliche Einschränkungen anzuwenden. Da die Knoten in einem Katalog Beschaffungskategorien sind, können sie durch eine Richtlinienregel für Kategoriezugriff unterdrückt werden. In diesem Fall werden die Produkte aus dieser Kategorie nicht zur Verfügung, und Mitarbeiter auf Anforderungen verwenden. Sie definieren Kategoriezugriffsrichtlinienregeln auf der Seite **Einkaufsrichtlinien**. In der folgenden Tabelle werden die Aufgaben beschrieben, die zum Einrichten eines Katalogs ausgeführt werden müssen.

| Aufgabe                                                   | Rolle             | Beschreibung                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dient zum Erstellen eines neuen Katalogs.                                  | Einkaufsvertreter | Beim Erstellen eines Katalogs geben Sie einen Namen und eine Beschreibung für den Katalog ein. Sie können auch festlegen, ob der Katalog manuell oder automatisch aktualisiert werden soll und den Katalogbesitzer angeben .                                                                                                                                      |
| Steuern Sie, ob Produkte im Katalog verfügbar sind. | Einkaufsvertreter | Da die Produkte aus den Beschaffungskategorien übernommen werden, werden sie alle in den entsprechenden Katalogknoten angezeigt. Sie können steuern, ob alle Produkte in einem Knoten ausgeblendet oder angezeigt werden, wenn der Katalog in einer Bestellanforderung verwendet wird. Sie können auch steuern, ob Einzelprodukte in einem Knoten ausgeblendet oder angezeigt werden. |
| Veröffentlichen Sie einen Katalog.                                   | Einkaufsvertreter | Bevor ein Katalog Mitarbeitern für Anforderungen zur Verfügung steht, müssen Sie eine Katalogrichtlinienregel für den Katalog definieren, den Status des Katalogs auf **Aktiv** setzen und den Katalog veröffentlichen. Sie können Kataloge, die nicht mehr für Benutzer verfügbar sein sollen, deaktivieren.                                              |

Aktualisierungen werden entweder automatisch oder manuell veröffentlicht. Dies hängt von der Option ab, die Sie für den Katalog im Feld **Standardmäßiger Aktualisierungstyp** der Seite **Kataloge** ausgewählt haben. Für Kataloge stehen die folgenden standardmäßigen Aktualisierungstypen zur Verfügung:

-   **Dynamisch** – Der Katalog wird automatisch aktualisiert, wenn an ihm eine Änderung vorgenommen wird.
-   **Statisch** – Der Katalog muss manuell aktualisiert werden.
-   **Beides** – Wenn der Katalog Produktkategorien beinhaltet, die den standardmäßigen Aktualisierungstyp **Statisch** aufweisen, müssen bei einer Aktualisierung diese Kategorien manuell aktualisiert werden. Kataloge mit Produktkategorien, die den standardmäßigen Aktualisierungstyp **Dynamisch** aufweisen, werden automatisch aktualisiert, wenn am Katalog eine Änderung vorgenommen wird.


<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Beschaffungskategoriehierarchie einrichten](tasks/set-up-procurement-category-hierarchy.md)



