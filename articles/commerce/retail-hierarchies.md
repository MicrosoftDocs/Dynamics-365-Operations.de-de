---
title: Hierarchien in Commerce
description: In diesem Artikel werden Hierarchien in Dynamics 365 Commerce beschrieben.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.industry: Retail
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
ms.openlocfilehash: ce196acc8c4bced865b983b12d72f8bc6e4d02a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271876"
---
# <a name="commerce-hierarchies"></a>Hierarchien in Commerce

[!include [banner](includes/banner.md)]

In diesem Artikel werden Hierarchien in Dynamics 365 Commerce beschrieben.

Sie können eine Kategoriehierarchie erstellen, um die Produkte zu organisieren, die Sie über die Kanäle verkaufen. Sie können Produkthierarchien verwenden, um Produkte zu kategorisieren oder zu gruppieren. Sie können diese Produkte dann verwenden, um Produktsortimente und Debitortreueprogramme zu erstellen. Sie können auch Produktattribute und Eigenschaften zuweisen, eine Preisgestaltungsstruktur zuweisen, die Produkte in verkaufsfördernde Maßnahmen einschließen und die Produkte für Berichte verwenden. Sie können eine Kategoriehierarchie erstellen, um alle Produkte und Kategorien in der Organisation darzustellen, und diese Kategoriehierarchie anschließend für mehrere Zwecke verwenden. Alternativ können Sie mehrere Kategoriehierarchien zu bestimmten Zwecken wie beispielsweise verkaufsfördernden Maßnahmen erstellen. Wenn Sie eine Produkthierarchie erstellen, müssen Sie einen Kategoriehierarchietyp zuweisen, um den Zweck der Kategoriehierarchie zu kennzeichnen. Beispielsweise werden nur Produkthierarchien, die dem Typ **Commerce-Navigationshierarchie** zugewiesen sind, referenziert, wenn Sie Produkte nach der Kategorie online oder in POS suchen.

## <a name="hierarchy-types"></a>Hierarchietypen

In der folgenden Tabelle werden die Typen von verfügbaren Kategoriehierarchien und der allgemeine Zweck der einzelnen Typen aufgelistet.

| Kategoriehierarchietyp       | Zweck |
|-------------------------------|---------|
| Produkthierarchie      | Verwenden Sie diesen Hierarchietyp, um die Gesamtprodukthierarchie für Ihre Organisation zu definieren. Sie können diesen Hierarchietyp für den Verkauf, die Preisgestaltung und die verkaufsfördernden Maßnahmen, die Berichterstellung und die Sortimentsplanung verwenden. Dieser Hierarchietyp kann nur einer Produkthierarchie zugewiesen werden. |
| Zusätzliche Hierarchie | Verwenden Sie diesen Hierarchietyp für alle weiteren Kategoriehierarchien, die Sie erstellen möchten. Im Frühjahr können Sie beispielsweise eine verkaufsfördernde Maßnahme für Badebekleidung erstellen. Daher schließen Sie die Badebekleidungsprodukte in einer separaten Kategoriehierarchie ein und wenden die Preisgestaltung der verkaufsfördernden Maßnahme auf die verschiedenen Produktkategorien an. |
| Navigationshierarchie   | Verwenden Sie diesen Hierarchietyp, um Produkte in Kategorien zu gruppieren und zu organisieren, damit die Produkte online oder in POS gesucht werden können. |

Durch Verwenden einer Kategoriehierarchie zum Strukturieren der Produkte können Sie Produktattribute und Eigenschaften auf Kategorieebene einrichten und warten. Diese Attribute und Eigenschaften umfassen Einstellungen für Produktdimensionen und Point-of-Sale-Einstellungen (POS). Alle Produkte, die den Kategorien zugewiesen werden, erben automatisch die Attribute und Eigenschaften, die Sie definieren. Sie können die Eigenschaftseinstellungen für ein beliebiges Produkt auf mehrere Produkte in einer ausgewählten Kategorie gleichzeitig kopieren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
