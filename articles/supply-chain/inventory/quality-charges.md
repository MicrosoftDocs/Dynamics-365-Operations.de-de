---
title: Belastungen für Qualitätsmangel-Vorgänge
description: Dieses Thema beschreibt, wie Sie Qualitätsbelastungen erstellen, die mit Vorgängen für eine Nichtkonformität verwendet werden können.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022299"
---
# <a name="charges-for-nonconformance-operations"></a>Belastungen für Qualitätsmangel-Vorgänge

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Sie Qualitätsbelastungen erstellen, die mit Vorgängen für eine Nichtkonformität verwendet werden können.

Sie verwenden die Seite **Qualitätsbelastungen**, um die Arten von Belastungen zu definieren, die zu Vorgängen für einen Qualitätsmangel hinzugefügt werden können. Mit Belastungen können Sie Details zu Gebühren oder Kosten verfolgen, die Sie einem Debitor für Qualitätsmängel schulden oder die ein Kreditor Ihnen für erhaltene Qualitätsmängel schuldet. Sie könnten auch Belastungen verwenden, um Kosten zu verfolgen, die für externe Kreditor oder Dienstleistungen zur Durchführung eines Vorgangs erforderlich sind.

## <a name="examples-of-quality-charges"></a>Beispiele für Qualitätsbelastungen

Sie arbeiten für eine produzierende Firma. Ihre Firma hat Verträge mit mehreren Kreditor. In diesen Verträgen werden Standards für die pünktliche Lieferung, Schäden und Produktqualität von Elementen festgelegt. Ebenso haben mehrere Ihrer Debitoren Vereinbarungen mit Ihrer Firma über Retouren, Schäden und Produktqualität.

Eine Gebührenstruktur wird für jeden Umstand definiert und im Vertrag festgelegt. Sie können Qualitätsbelastungen konfigurieren, um die verschiedenen Arten von Belastungen zu umreißen, z. B. *Schäden*, *Verspätete Lieferung* und *Qualität*. Wenn Sie dann einen Qualitätsmangel erstellen, fügen Sie einen oder mehrere Vorgänge hinzu. Für jeden Vorgang wählen Sie **Gebühren**, um die Details zu den Gebühren zu definieren.

## <a name="create-a-quality-charge"></a>Erstellen Sie eine Qualitätsgebühr

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Qualitätsbelastungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Belastungen code** – Geben Sie eine eindeutige ID oder einen Namen für die Qualitätsgebühr ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Qualitätsgebühr ein.

1. Schließen Sie die Seite.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Fügen Sie eine qualitative Belastung zu einem Vorgang für einen Qualitätsmangel hinzu

Details darüber, wie Sie Vorgänge zu einem Qualitätsmangel hinzufügen und ihnen Belastungen zuweisen, finden Sie unter [Vorgänge für Qualitätsmängel](quality-operations.md).

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
