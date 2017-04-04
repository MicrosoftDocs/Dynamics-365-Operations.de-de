---
title: Bilanzfinanzberichte
description: "In diesem Artikel wird beschrieben Standardberichte die für Bilanzen. Er wird zudem beschrieben die Bausteine, die mit diesen Berichten zugeordnet werden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 664d32c2bfecb50e24fd48a66ab5b34cef6c09a3
ms.lasthandoff: 03/31/2017


---

# <a name="balance-sheet-financial-reports"></a>Bilanzfinanzberichte

In diesem Artikel wird beschrieben Standardberichte die für Bilanzen. Er wird zudem beschrieben die Bausteine, die mit diesen Berichten zugeordnet werden. 

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

 

<a name="see-also"></a>Siehe auch
--------

[Financial reporting](financial-reporting-getting-started.md)

[View financial reports](view-financial-reports.md)

[Dynamics-Rechnungslegungs-Blog (http://blogs.msdn.com/b/dynamics_financial_reporting/)]


