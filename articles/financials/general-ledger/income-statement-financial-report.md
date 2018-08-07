---
title: "Finanzbericht für die Einkommensaufstellung"
description: "In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9310508082ff710cd040b74519044f5a90c23988
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

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

[Dynamics Financial Reporting-Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)




