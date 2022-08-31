---
title: Quarantänezonen für Qualitätsmängel
description: Dieser Artikel beschreibt, wie Sie Quarantänezonen für Qualitätsmängel erstellen und verwenden.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e556d2aa078a76ff4f81b6763535c38ce1cca0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857705"
---
# <a name="quarantine-zones-for-nonconformances"></a>Quarantänezonen für Qualitätsmängel

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Quarantänezonen für Qualitätsmängel erstellen und verwenden.

Sie verwenden die Seite **Quarantänezonen**, um Zonen zu definieren, die Qualitätsmängeln zugeordnet werden können. Wenn Sie einen Qualitätsmangel erstellen, können Sie die Felder **Quarantänezone** und **Quarantänetyp** auf der Registerkarte **Allgemein** der Seite **Nichtkonformitäten** festlegen. Das Feld **Quarantänezone** gibt normalerweise den Bereich oder Lagerplatz an, in dem sich das Element befindet. Das Feld **Quarantänetyp** definiert das Element entweder als *Eingeschränkte Verwendung* oder *Unverwendbar*.

Wenn Sie einen Bericht über Qualitätsmängel oder Korrekturen für einen Qualitätsmangel drucken, können Sie die Quarantänezone anzeigen, in der sich das Element befindet.

Sie können auch ein Etikett für einen Qualitätsmangel drucken. Dieser Bericht zeigt die zugewiesene Quarantänezone und Informationen über die Verwendung an, um Anhaltspunkte für den Umgang mit defektem Material zu geben. Die Quarantänezonen können Lagerplätzen oder Vorgängen entsprechen.

## <a name="examples-of-quarantine-zones"></a>Beispiele für Quarantänezonen

### <a name="example-1"></a>Beispiel 1

Sie arbeiten bei einer Firma, die Elektronik herstellt und Fernsehgeräte, Lautsprecher und Media Player produziert und vertreibt. In diesem Fall können Sie eine Quarantänezone konfigurieren, die jeden Produkttyp repräsentiert.

### <a name="example-2"></a>Beispiel 2

Drei Behälter und zwei Regale dienen zur Aufbewahrung von Elementen, die nicht den Qualitätsanforderungen entsprechen. In diesem Fall können Sie fünf Quarantänezonen konfigurieren, eine für jeden Behälter und jedes Regal.

## <a name="create-a-quarantine-zone"></a>Erstellen Sie eine Quarantänezone

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätsmanagement \> Quarantänezonen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Quarantänezone** – Geben Sie eine eindeutige ID oder einen Namen für die Quarantänezone ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Quarantänezone ein.

1. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist](quality-responsible-workers.md)
- [Problemtypen für Qualitätsmängel](quality-quarantine-zones.md)
- [Diagnosetypen für Qualitätsmängel](quality-diagnostic-types.md)
- [Qualitätsbelastungen für Qualitätsmängel](quality-charges.md)
- [Vorgänge für Qualitätsmängel](quality-operations.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
