---
title: Problemtypen für Qualitätsmängel
description: Dieser Artikel beschreibt, wie Sie Problemtypen für Qualitätsmängel erstellen und verwenden.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a73e692257c2a27085d60e75e028445811ee778a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857749"
---
# <a name="problem-types-for-nonconformances"></a>Problemtypen für Qualitätsmängel

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Problemtypen für Qualitätsmängel erstellen und verwenden.

Sie verwenden die Seite **Problemtypen**, um eine Klassifizierung der Qualitätsprobleme zu definieren, die bei den verschiedenen Qualitätsmangel-Typen auftreten können. Für jeden Problemtyp, den Sie erstellen, müssen Sie die Arten von Qualitätsmängeln angeben, mit denen der Problemtyp verwendet werden kann. Sie können die folgenden Arten von Qualitätsmängeln festlegen:

- **Intern** – Qualitätsmängel dieses Typs beziehen sich auf den Lagerbestand (z. B. Qualitätsprüfungsaufträge oder Quarantäneaufträge).
- **Kunde** – Qualitätsmängel dieser Art beziehen sich auf Kundenaufträge.
- **Lieferant** – Qualitätsmängel dieser Art beziehen sich auf Einkaufsbestellungen.
- **Serviceanfrage** – Qualitätsmängel dieser Art beziehen sich auf Serviceaufträge.
- **Produktion** – Qualitätsmängel dieser Art beziehen sich auf Batch-Aufträge oder Produktionsaufträge.
- **Kuppelprodukt-Produktion** – Qualitätsmängel dieser Art beziehen sich auf Batch-Aufträge für Kuppelprodukte.

Wenn Sie einen neuen Problemtyp erstellen, wählen Sie **Qualitätsmangel-Typen** im Aktivitätsbereich, um eine Liste mit einem oder mehreren Qualitätsmangel-Typen zu erstellen, die für den Problemtyp zugelassen sind. Ein Problemtyp, der sich auf einen Fehlercode bezieht, kann beispielsweise für alle Qualitätsmängel gelten. Ein Problemtyp, der sich auf Reklamationen von Debitor bezieht, kann jedoch nur für die Typen **Kunde** und **Serviceanfrage** Qualitätsmangel gelten.

## <a name="examples-of-problem-types"></a>Beispiele für Problemtypen

Hier sind einige Beispiele für Szenarien für Problemtypen, die mit den verschiedenen Qualitätsmängeln verwendet werden können:

- **Kunde:** Ein Kunde hat eine Beschwerde eingereicht, ein Kunde hat eine Rücksendung gemacht, oder die Qualitätsvorgaben wurden nicht erfüllt.
- **Lieferant:** Das Produkt war beschädigt, die Qualitätsspezifikationen wurden nicht erfüllt oder es wurde das falsche Produkt geliefert.
- **Serviceanfrage:** Qualitätsvorgaben wurden nicht eingehalten, ein Kunde hat sich beschwert oder eine Maschinenwartung ist erforderlich.
- **Produktion:** Die Qualitätsvorgaben wurden nicht erfüllt, eine Maschinenwartung ist erforderlich oder das Produkt wurde beschädigt.
- **Kuppelprodukt-Produktion:** Die Qualitätsvorgaben wurden nicht eingehalten, eine Maschinenwartung ist erforderlich oder das Produkt wurde beschädigt.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Erstellen Sie einen Problemtyp und ordnen Sie ihn Qualitätsmängeln zu

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätsmanagement \> Problemtypen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Problemtyp** – Geben Sie eine eindeutige ID oder einen Namen für den Problemtyp ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des Problemtyps ein.

1. Während die neue Zeile noch ausgewählt ist, wählen Sie **Nicht konforme Typen** im Aktivitätsbereich.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie dann für die neue Zeile das Feld **Qualitätsmangel-Typ** auf den Qualitätsmangel-Typ fest, den Sie für den Problemtyp zulassen wollen.
1. Wiederholen Sie den vorherigen Schritt für jede zusätzliche Qualitätsmangel-Art, die Sie für die Problemart zulassen wollen.
1. Schließen Sie die Seiten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist](quality-responsible-workers.md)
- [Quarantänezonen für Qualitätsmängel](quality-quarantine-zones.md)
- [Diagnosetypen für Qualitätsmängel](quality-diagnostic-types.md)
- [Qualitätsbelastungen für Qualitätsmängel](quality-charges.md)
- [Vorgänge für Qualitätsmängel](quality-operations.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
