---
title: Diagnosetypen für Qualitätsmängel
description: Dieses Thema beschreibt, wie Sie Diagnosetypen verwenden und erstellen, die mit Qualitätsmängeln verwendet werden können.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 560627bf5ecd38f3fc79448629390acb549e40fb1388958d9eac094517925039
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781512"
---
# <a name="diagnostic-types-for-nonconformances"></a>Diagnosetypen für Qualitätsmängel

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Sie Diagnosetypen verwenden und erstellen, die mit Qualitätsmängeln verwendet werden können.

Sie verwenden die Seite **Diagnosetypen**, um eine Klassifizierung von Diagnoseaktionen zu definieren. Wenn Sie dann eine Korrektur für einen Qualitätsmangel erstellen, wählen Sie eine Diagnose aus. Durch eine Korrektur werden die Diagnoseaktivität für eine genehmigte Nichtübereinstimmung sowie die ausführende Person angegeben. Außerdem werden das angeforderte und das geplante Abschlussdatum angezeigt.

## <a name="examples-of-diagnostic-types"></a>Beispiele für Diagnosetypen

Sie arbeiten für eine produzierende Firma, und mehrere Elemente haben Qualitätstests nicht bestanden. Diese Elemente werden in einen Quarantänebereich verschoben und als Qualitätsmangel gekennzeichnet. Ein Datensatz für Qualitätsmängel wird in Microsoft Dynamics 365 Supply Chain Management erstellt, um die Details bis zur Problemlösung zu verfolgen.

In diesem Fall treten die Qualitätsprobleme auf, weil Lager in der Maschine, die die Elemente verpackt, schlecht geworden sind und sich überhitzen. Die Korrektur für dieses Problem ist der Austausch der Teile in der Maschine.

Wenn Sie die Diagnosetypen konfigurieren, können Sie mehrere Datensätze erstellen, von denen jeder eine andere Art von Problem darstellt, das die Maschine haben könnte. Alternativ können Sie einen generischen Diagnosetyp erstellen, der eine Maschinenreparatur darstellt.

## <a name="create-a-diagnostic-type"></a>Erstellen Sie einen Diagnosetyp

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Diagnosetypen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Diagnose** – Geben Sie eine eindeutige ID oder einen Namen für den Diagnosetyp ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Diagnoseart ein.

1. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist](quality-responsible-workers.md)
- [Quarantänezonen für Qualitätsmängel](quality-quarantine-zones.md)
- [Problemtypen für Qualitätsmängel](quality-problem-types.md)
- [Qualitätsbelastungen für Qualitätsmängel](quality-charges.md)
- [Vorgänge für Qualitätsmängel](quality-operations.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
