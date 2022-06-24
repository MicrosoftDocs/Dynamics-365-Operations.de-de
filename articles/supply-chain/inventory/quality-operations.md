---
title: Vorgänge für Qualitätsmängel
description: In diesem Artikel wird beschrieben, wie Sie Vorgänge für Qualitätsmängel erstellen und verwenden.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e63156dd2b230da7f1ea89e2c2006c1b4f3eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847990"
---
# <a name="operations-for-nonconformances"></a>Vorgänge für Qualitätsmängel

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Vorgänge für Qualitätsmängel erstellen und verwenden.

Sie können die Seite **Vorgänge** verwenden, um Klassifizierungen der Arbeiten zu definieren, die für einen genehmigten Qualitätsmangel durchgeführt werden können. Wenn Sie einem Qualitätsmangel einen zugehörigen Vorgang zuweisen, können Sie Details wie das zugehörige Material, die Arbeitsstunden und die Belastungen angeben, die für die Durchführung des Vorgangs erforderlich sind. Anhand dieser Informationen berechnet das System eine Kalkulation für den Vorgang. Die ausführlichen Informationen sowie die vorkalkulierten Kosten dienen lediglich zu Referenzzwecken. Die zugehörigen Arbeitsgänge für die Qualität unterscheiden sich von den Arbeitsgängen, die für einen Produktionsarbeitsplan definiert werden können.

> [!NOTE]
> Obwohl Sie Kosten, Zeit und die Elemente verfolgen können, die in einem Vorgang verwendet werden, der mit einem Qualitätsmangel zusammenhängt, haben die von Ihnen eingegebenen Daten nur informativen Charakter. Es ist nicht automatisch mit dem Hauptbuch, dem untergeordneten Sachkonto oder dem Modul **Zeiterfassung** integriert.

## <a name="examples-of-operations"></a>Beispiele für Vorgänge

Sie arbeiten für eine produzierende Firma. Ein Qualitätsmangel wurde für Elemente erstellt und genehmigt, die einen Qualitätstest nicht bestanden haben. Eine Korrektur wurde erstellt, um anzuzeigen, dass das Problem mit einem schlechten Lager an einer Maschine zusammenhängt. Für den Austausch des Lagers sind mehrere Schritte erforderlich, und die Verantwortung für jeden Vorgang wird nachverfolgt. Zum Beispiel könnten die folgenden Schritte erforderlich sein:

1. Die Zeile wird gestoppt und die Bereinigungsroutine wird durchgeführt.
1. Wartungspersonal tauscht das Lager aus.
1. Qualitätssicherungspersonal inspiziert die Maschine, bevor sie wieder eingeschaltet wird.

Für dieses Beispiel können die folgenden Vorgänge erstellt werden, um die zu erledigende Arbeit darzustellen:

- Stoppen Sie die Produktionslinie.
- Bereinigen Sie die Produktionszeile.
- Maschinenwartung durchführen.
- Inspizieren Sie die Maschine.

## <a name="create-an-operation"></a>Erzeugen eines Vorgangs

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Vorgänge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Vorgang** – Geben Sie eine eindeutige ID oder einen Namen für den Vorgang ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des Vorgangs ein.
    - **Typ** – Wenn der Vorgang nur bei Qualitätsmängeln verwendet werden kann, die sich auf einen bestimmten Auftragstyp beziehen, wählen Sie den Auftragstyp (*Einkaufsbestellung* oder *Verkaufsauftrag*).

1. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Erstellen und verarbeiten Sie Qualitätsmängel](tasks/create-process-non-conformance.md)
- [Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist](quality-responsible-workers.md)
- [Quarantänezonen für Qualitätsmängel](quality-quarantine-zones.md)
- [Diagnosetypen für Qualitätsmängel](quality-diagnostic-types.md)
- [Qualitätsbelastungen für Qualitätsmängel](quality-charges.md)
- [Problemtypen für Qualitätsmängel](quality-operations.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
