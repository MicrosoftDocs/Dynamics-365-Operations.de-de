---
title: Finanzbericht für die Einkommensaufstellung
description: In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177864"
---
# <a name="income-statement-financial-report"></a>Finanzbericht für die Einkommensaufstellung

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden. 

<a name="default-income-statement-report"></a>Standardbericht für die Einkommensaufstellung
-------------------------------

| Standardbericht             | Funktionsweise                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Einkommensaufstellung – Standard | Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn. |

## <a name="building-blocks"></a>Bausteine
Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.

| Standardbericht             | Zeilendefinition                     | Spaltendefinition          |
|----------------------------|------------------------------------|----------------------------|
| Einkommensaufstellung - Standard | Zusammengefasste Einkommensaufstellung - Standard | Periodisch und seit Jahresbeginn - Standard |

### <a name="row-definition"></a>Zeilendefinition

Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung. Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen. Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.

### <a name="column-definition"></a>Spaltendefinition

Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.

-   **Periodisch und seit Jahresbeginn - Standardspaltentypen:**
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **FD** - Finanzdaten für die aktuelle Periode
    -   **FD** - Finanzdaten seit Jahresbeginn



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Finanzberichterstellung](financial-reporting-getting-started.md)

[Finanzberichte anzeigen](view-financial-reports.md)

[Dynamics Financial Reporting-Blog](https://blogs.msdn.com/b/dynamics_financial_reporting/)


