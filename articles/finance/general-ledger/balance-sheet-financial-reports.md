---
title: Bilanzfinanzberichte
description: In diesem Artikel werden die Standardberichte für Bilanzen beschrieben. Er beschreibt zudem die die Bausteine, die diesen Berichten zugeordnet werden.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177876"
---
# <a name="balance-sheet-financial-reports"></a>Bilanzfinanzberichte

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Standardberichte für Bilanzen beschrieben. Er beschreibt zudem die die Bausteine, die diesen Berichten zugeordnet werden. 

<a name="default-balance-sheet-reports"></a>Standardbilanzberichte
-----------------------------

Es gibt zwei Standardbilanzberichte. Bei einem Bericht werden die Abschnitte gestapelt. Beim anderen Bericht sind die Abschnitte parallel.

| Standardbericht                       | Funktionsweise                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Bilanz – Standard              | Enthält eine Ansicht der Finanzposition der Organisation während des Jahres.                                                                 |
| Parallele Bilanz – Standard | Enthält eine Ansicht der Finanzposition der Organisation während des Jahres. Aktiva und Passiva und Eigenkapital sind parallel. |

## <a name="building-blocks"></a>Bausteine
Die Bilanzfinanzberichte verwenden die folgenden Bausteine.

| Standardbericht                       | Zeilendefinition                       | Spaltendefinition             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Bilanzberichte - Standard              | Bilanzberichte - Standard              | YTD und Abweichung - Standard    |
| Parallele Bilanz – Standard | Parallele Bilanz – Standard | Seit Jahresbeginn-Spalte - Standard |

### <a name="row-definition"></a>Zeilendefinition

Die Zeilendefinitionen für beide Bilanzberichte enthalten Abschnitte für jeden Teil einer herkömmlichen Bilanz. Der parallele Bericht umfasst einen Spaltenumbruch, damit Verbindlichkeiten und das Eigenkapital neben Anlagen angezeigt wird. Die Hauptkontokategoriedimension wird verwendet, um beide Zeilendefinitionen aufzubauen. Daher kann jeder Benutzer die Berichte erstellen, ohne Änderungen vorzunehmen zu müssen.

### <a name="column-definition"></a>Spaltendefinition

Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.

-   **YTD und Abweichung - Standardspaltentypen:**
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **FD** - Die Finanzdaten seit Jahresbeginn für das aktuelle Jahr
    -   **FD** - Die Finanzdaten seit Jahresbeginn für das letzte Jahr
    -   **CALC** - Die Abweichung aus der Subtraktion des letzten Jahres von diesem Jahr

<!-- -->

-   **Seit Jahresbeginn-Spalte - Standard:**
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **FD** - Die Finanzdaten seit Jahresbeginn für das aktuelle Jahr



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Finanzberichterstellung](financial-reporting-getting-started.md)

[Finanzberichte anzeigen](view-financial-reports.md)

[Dynamics Financial Reporting-Blog](https://blogs.msdn.com/b/dynamics_financial_reporting/)



