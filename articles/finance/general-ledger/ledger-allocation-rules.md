---
title: Sachkonto-Zuordnungsregeln
description: Dieser Artikel enthält Informationen zu Sachkonto-Zuordnungsregeln. Er beschreibt die verschiedenen Komponenten dieser Zuordnungsregeln und der Zuordnungsmethoden, die für sie verwendet werden können.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acd91f9343e3d3a77d2cc32bc8b6c2d6469430477eed0c3b62e1e699cd6816e9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780409"
---
# <a name="ledger-allocation-rules"></a>Sachkonto-Zuordnungsregeln

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Sachkonto-Zuordnungsregeln. Er beschreibt die verschiedenen Komponenten dieser Zuordnungsregeln und der Zuordnungsmethoden, die für sie verwendet werden können.

Sachkonto-Zuordnungsregeln werden verwendet, um Zuordnungserfassungen und Kontoeinträge für die Zuordnung von Sachkontosalden oder -festen Beträgen automatisch zu berechnen und zu generieren. Zuordnungsmethoden können variabel oder fest sein. Folgende Zuordnungsmethoden können für Sachkontozuordnungsregeln verwendet werden:

-   **Basis** - Diese variable Methode wird verwendet, wenn die Verteilung vom tatsächlichen Sachkontensaldo abhängt (auf Grundlage von Filterkriterien). Beispielsweise können Werbeausgaben eines Unternehmens zum Umsatz der einzelnen Abteilungen und dem Gesamtumsatz aller Abteilungen zugeordnet werden.
-   **Fester Prozentsatz** und **Festes Gewicht** – Für diese Methoden werden der Prozentsatz oder das Gewicht direkt für die Regel definiert. Beispielsweise können Werbekosten zugewiesen werden, damit Abteilung A 70 Prozent der Werbeausgaben zugeordnet werden und Abteilung B 30 Prozent zugeordnet werden.
-   **Gleich** – Diese Methode verteilt den Betrag gleichmäßig jedem definierten Ziel. Wenn beispielsweise Ziele für Abteilung A und Abteilung B definiert werden, können Werbekosten so zugewiesen werden, das Abteilung A und Abteilung B 50 Prozent der Werbeausgaben empfangen.

Ist die Zuordnungsmethode Basis als Zuordnungsregel festgelegt ist, muss außerdem eine separate Basisregel für die Sachkontozuordnung erstellt werden. Der Prozess "Zuordnungsanforderung verarbeiten" bietet Benutzer die Möglichkeit Sachkontozuordnungsregel verarbeiten und die resultierenden Zuordnungserfassungseinträge in der Vorschau anzeigen, bevor sie entweder die berechneten Zuweisungen buchen oder löschen.

## <a name="components-of-ledger-allocation-rules"></a>Komponenten von Zuweisungserfassungsregeln
Jede Zuordnungsregel besitzt vier Komponenten: Allgemeines, Quelle, Ziel und Gegenkonto. Eine zusätzliche Komponente, die Sachkontozuordnungsbasisregel, ist erforderlich, wenn "Basis" als Zuordnungsmethode verwendet wird. Jede Komponente enthält eine entscheidende Information, die für die Verarbeitung der Zuordnungen erforderlich sind.

-   **Allgemein** – In dieser Komponente gibt der Benutzer Optionen wie die Zuordnungsmethode, Intercompany-Regeleinstellungen und den Bestimmungsbereich der Regel ein.
-   **Quelle** – Diese Komponente dient zur Angabe der Quelldaten für die Zuordnung durch den Benutzer. Zuteilung können auf Sachkontosalden (**Datenquelle** = **Sachkonto**) oder feste Beträge basieren (**Datenquelle** = **Fester Wert**). Wenn **Datenquelle** auf **Sachkonto** festgelegt ist, müssen Quellfilterkriterien für die Sachkontozuordnungsregel definiert werden (beispielsweise für die Werbekosten).
-   **Ziel** – Mithilfe dieser wird definiert, wie das Ergebnis der Zuweisungsberechnung auf die verteilt und aufgeteilt werden soll. Beispielsweise kann es eine Zielposition für jede Abteilung geben.
-   **Gegenkonto** – Diese Komponente definiert, wie Hauptkonten und Dimensionen für die Gegenbuchungen bestimmt werden, die die Zieleinträge ausgleichen. Benutzerdefinierte Optionen werden in der Regel anstelle von Konten und Dimensionen auf Quellbasis verwendet. Wenn **Datenquelle** auf **Fester Wert** festgelegt ist, kann **Quelle** nicht als Option verwendet werden.
-   **Sachkontozuteilungsbasisregeln** – Diese Regeln verwenden ihre eigenen Quellfilterkriterien, um festzulegen, welche Sachkontosalden für die Zuweisung verwendet werden sollen (beispielsweise, Umsatzerlös pro Abteilung). Jede Zuordnungsbasisregel kann für eine Vielzahl von Zuordnungsregeln verwendet werden.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]