---
title: Anlagenservicelevel
description: In diesem Thema werden Anlagenservicelevel in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e2f8d2ac0c48d4f92b15ec345ffa650b71df0b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571023"
---
# <a name="asset-service-levels"></a>Anlagenservicelevel

[!include [banner](../../includes/banner.md)]

 

In diesem Thema werden Anlagenservicelevel in Asset Management erläutert. Anlagenservicelevel beziehen sich auf Anlagen und werden auf Wartungsanfragen und Arbeitsaufträge übertragen. Sie werden verwendet, um die Priorität von Arbeitsaufträgen während der Arbeitsauftragsplanung zu berechnen. Anlagenservicelevel können geändert werden, wenn Änderungen erforderlich sind.

Weitere Informationen zu den Einstellungen, die sich auf die Berechnung von Bewertungsnoten für Arbeitsauftragsplanung beziehen, finden Sie unter [Anlagenverwaltungsparameter](../setup-for-objects/enterprise-asset-management-parameters.md). Sie müssen mindestens einen Standarddatensatz für den Anlagenservicelevel einrichten. Dieser Standarddatensatz wird verwendet, wenn keine andere Übereinstimmung während der Arbeitsauftragsplanung gefunden wird.

**Beispiel 1:** Der Standardservicelevel, der verwendet wird, wenn keine andere Übereinstimmung gefunden wird. In diesem Datensatz wählen Sie nur einen Servicelevel aus.

**Beispiel 2:** Ein hoher Servicelevel, der verwendet wird, um einen Wartungseinzelvorgang für einen Volvo-Lkw-Motor zu planen. In diesem Datensatz wählen Sie einen entsprechenden Anlagentypen aus, wie z. B. **Lkw-Motor**, einen Hersteller (**Volvo**) und eine Servicelevel.

## <a name="set-up-asset-service-levels"></a>Anlagenservicelevel einrichten

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagenservicelevel**.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Je nach der Detailebene, die für den Anlagenservicelevel erforderlich ist, nehmen Sie die entsprechende Auswahl in den Feldern **Funktionaler Standort**, **Anlagentyp**, **Hersteller**, **Modell**, **Anlage**, **Arbeitsauftragstyp** und **Servicelevel** vor.

    > [!NOTE]
    > Wenn der Anlagenservicelevel für Wartungsanfragen und Arbeitsaufträge verwendet wird, durchläuft Asset-Management alle Anlagenservicelevel-Datensätze, um nach einer möglichen Übereinstimmung zu suchen. Die spezifischste Kombination wird immer zuerst geprüft. Das bedeutet, Asset Management sucht als Erstes nach einer Übereinstimmung für das Feld **Arbeitsauftragstyp**. Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Anlage** usw. Wie Sie im Layout der Seite **Anlagenservicelevel** sehen können, bedeutet dieses Verhalten, dass Asset Management zum Auffinden der spezifischsten Kombinationen jeden Datensatz von rechts nach links auf Übereinstimmung prüft. Wenn keine Übereinstimmung gefunden wird, wird der Standarddatensatz, der keine Auswahl in diesen Feldern hat, verwendet.

4. Wählen Sie im Feld **Servicelevel** eine Zahl aus, die den Servicelevel (die Priorität) angibt.


> [!NOTE]
> Wenn Sie einen Anlagenservicelevel-Datensatz auf der Seite ändern **Anlagenservicelevel** ändern, nachdem Sie ihn bereits für einen Arbeitsauftrag verwendet haben, wird der Servicelevel für Wartungsanfragen und Arbeitsaufträge nicht entsprechend aktualisiert.
