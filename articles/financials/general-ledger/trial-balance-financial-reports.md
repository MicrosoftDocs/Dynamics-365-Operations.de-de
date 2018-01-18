---
title: Zwischenbilanzfinanzberichte
description: "In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben. Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6d5674bed7167e002e7467e1e77d333fdf1b4f8d
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="trial-balance-financial-reports"></a>Zwischenbilanzfinanzberichte

[!include[banner](../includes/banner.md)]


In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben. Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen. 

<a name="default-trial-balance-reports"></a>Standardzwischenbilanzberichte
-----------------------------

Drei Zwischenbilanzberichte sind in der Finanzberichterstellung von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition verfügbar.

| Standardbericht                                 | Funktionsweise                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ausführliche Zwischenbilanz – Standard               | Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.                  |
| Zusammengefasste Zwischenbilanz – Standard                | Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.                                        |
| Jährlich zusammengefasste Zwischenbilanz – Standard | Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein. |

## <a name="building-blocks"></a>Bausteine
Die Zwischenbilanzfinanzberichte verwenden die folgenden Bausteine.

| Standardbericht                                 | Zeilendefinition          | Spaltendefinition                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Ausführliche Zwischenbilanz – Standard               | Zwischenbilanz - Standard | Ausführliche Zwischenbilanz – Standard               |
| Zusammengefasste Zwischenbilanz – Standard                | Zwischenbilanz - Standard | Zusammengefasste Zwischenbilanz - Standard                |
| Jährlich zusammengefasste Zwischenbilanz – Standard | Zwischenbilanz - Standard | Jährlich zusammengefasste Zwischenbilanz - Standard |

### <a name="row-definition"></a>Zeilendefinition

Die Zeilendefinition, Zwischenbilanz – Standard, enthält eine einzelne Zeile, die alle Hauptkonten übernimmt. Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen. Wenn Sie den Bericht anzeigen, führen Sie einen Drilldown der Einzelzeile durch, um Details zu jedem Konto zu sehen. Sie können die Zeilendefinition ändern, sodass sie weitere Details umfasst. Um die Zeilendefinition "Zwischenbilanz - Standard" zu ändern, sodass sie Zeilen für alle Konten umfasst, führen Sie die folgenden Schritte aus.

1.  Klicken Sie auf **Bearbeiten** und dann auf **Zeilen aus Dimensionen einfügen**. Mit dem Befehl **Zeilen aus Dimensionen einfügen** können Sie die Dimensionen auswählen, die Sie in Ihrer Zeile haben möchten. Für diese Zeilendefinition werden Sie **Hauptkonto** verwenden.
2.  Stellen Sie sicher, dass das **Hauptkonto** alle kaufmännischen Und-Zeichen (&) enthält, und klicken Sie auf **OK**.

Die Zeilendefinition enthält nun alle Hauptkonten für Ihres juristische Standardperson.

### <a name="column-definition"></a>Spaltendefinition

Jeder Zwischenbilanzbericht verwendet eine andere Spaltendefinition. Diese Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.

-   **Ausführliche Zwischenbilanz - Standardypaltentypen:**
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **ACCT** - Kontocodes
    -   **ATTR (3)** – Attribute:
        -   Buchungsdatum
        -   Beleg
        -   Erfassungsbeschreibung
    -   **FD** - Finanzdaten, die nur Soll enthalten
    -   **FD** - Finanzdaten, die nur Haben enthahlten
    -   **CALC** – Die Nettodifferenz
-   **Zusammengefasste Zwischenbilanz - Standardypaltentypen:**
    -   **ACCT** - Kontocodes
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **ATTR** – Ein Attribut:
        -   Beleg
    -   **FD** - Die Anfangssaldoenfinanzdaten
    -   **FD** - Finanzdaten, die nur Soll enthalten
    -   **FD** - Finanzdaten, die nur Haben enthahlten
    -   **CALC** – Die Nettodifferenz
    -   **CALC** – Der Abschlusssaldo
-   **Jährlich zusammengefasste Zwischenbilanz - Standard:**
    -   **ACCT** - Kontocodes
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **ATTR** – Ein Attribut
        -   Beleg
    -   **FD** - Die Anfangssaldoenfinanzdaten für das aktuelle Jahr
    -   **FD** - Finanzdaten, die nur Soll für das aktuelle Jahr enthahlten
    -   **FD** - Finanzdaten, die nur haben für das aktuelle Jahr entahlten
    -   **CALC** – Die Nettodifferenz
    -   **CALC** – Der Abschlusssaldo
    -   **FD** - Finanzdaten, die nur Soll für das letzte Jahr enthahlten
    -   **FD** - Finanzdaten, die nur Haben für das letzte Jahr enthalten

 

<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung](financial-reporting-getting-started.md)

[Finanzberichte anzeigen](view-financial-reports.md)

[Dynamics Financial Reporting-Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)




