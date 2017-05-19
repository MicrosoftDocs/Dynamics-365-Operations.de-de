---
title: Einzelhandelshierarchien
description: Dieser Artikel beschreibt die Einzelhandelshierarchien in Microsoft Dynamics AX.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4dc4fdfa8abf65ba13f5c94042a8eb28a3d7c046
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2017


---

# <a name="retail-hierarchies"></a>Einzelhandelshierarchien

[!include[banner](includes/banner.md)]


Dieser Artikel beschreibt die Einzelhandelshierarchien in Microsoft Dynamics AX.

Sie können eine Einzelhandelskategoriehierarchie erstellen, um die Produkte zu organisieren, die Sie über die Einzelhandelskanäle verkaufen. Sie können Einzelhandelsprodukthierarchien verwenden, um Produkte zu kategorisieren oder zu gruppieren. Sie können diese Produkte dann verwenden, um Produktsortimente und Debitortreueprogramme zu erstellen. Sie können auch Produktattribute und Eigenschaften zuweisen, eine Preisgestaltungsstruktur zuweisen, die Produkte in verkaufsfördernde Maßnahmen einschließen und die Produkte für Berichte verwenden. Sie können eine Einzelhandelskategoriehierarchie erstellen, um alle Produkte und Kategorien in der Organisation darzustellen, und diese Kategoriehierarchie anschließend für mehrere Zwecke verwenden. Alternativ können Sie mehrere Einzelhandelskategoriehierarchien zu bestimmten Zwecken, wie beispielsweise verkaufsfördernde Maßnahmen, erstellen. Wenn Sie eine Einzelhandelsprodukthierarchie erstellen, müssen Sie einen Kategoriehierarchietyp zuweisen, um den Zweck der Kategoriehierarchie zu kennzeichnen. Beispielsweise werden nur Produkthierarchien, die dem Typ **Einzelhandelsnavigationshierarchie** zugewiesen sind referenziert, wenn Sie Produkte nach der Kategorie online oder in POS suchen.

## <a name="retail-hierarchy-types"></a>Einzelhandelshierarchietypen
In der folgenden Tabelle werden die Typen von verfügbaren Einzelhandelskategoriehierarchien und der allgemeine Zweck der einzelnen Typen aufgelistet.

| Kategoriehierarchietyp       | Verwendungszweck                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Produkthierarchie (Einzelhandel)      | Verwenden Sie diesen Hierarchietyp, um die Gesamtprodukthierarchie für Ihre Organisation zu definieren. Sie können diesen Hierarchietyp für den Verkauf, die Preisgestaltung und die verkaufsfördernden Maßnahmen, die Berichterstellung und die Sortimentsplanung verwenden. Dieser Hierarchietyp kann nur einer Einzelhandelsprodukthierarchie zugewiesen werden.                                       |
| Zusätzliche Einzelhandelshierarchie | Verwenden Sie diesen Hierarchietyp für alle weiteren Einzelhandelskategoriehierarchien, die Sie erstellen möchten. Im Frühjahr können Sie beispielsweise eine verkaufsfördernde Maßnahme für Badebekleidung erstellen. Daher schließen Sie die Badebekleidungsprodukte in einer separaten Kategoriehierarchie ein und wenden die Preisgestaltung der verkaufsfördernden Maßnahme auf die verschiedenen Produktkategorien an. |
| Einzelhandelsnavigationshierarchie   | Verwenden Sie diesen Hierarchietyp, um Produkte in Kategorien zu gruppieren und zu organisieren, damit die Produkte online oder in POS gesucht werden können.                                                                                                                                                                                       |

Durch Verwenden einer Einzelhandelskategoriehierarchie zum Strukturieren der Produkte können Sie Produktattribute und Eigenschaften auf Kategorieebene einrichten und warten. Diese Attribute und Eigenschaften umfassen Einstellungen für Produktdimensionen und Point-of-Sale-Einstellungen (POS). Alle Produkte, die den Kategorien zugewiesen werden, erben automatisch die Attribute und Eigenschaften, die Sie definieren. Sie können die Eigenschaftseinstellungen für ein beliebiges Produkt auf mehrere Produkte in einer ausgewählten Kategorie gleichzeitig kopieren.




