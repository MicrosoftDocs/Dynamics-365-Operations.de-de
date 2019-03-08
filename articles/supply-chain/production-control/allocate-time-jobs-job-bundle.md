---
title: Zeit zu Einzelvorgängen in einer Stapelverarbeitung zuteilen
description: Sie können Einzelvorgänge in der Fertigungssteuerung bündeln. Sie können mehrere Einzelvorgänge auf der Seite "Einzelvorgangsliste" gleichzeitig starten.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33d6bab9beb28d18e2094d7fb5e670e9425aac39
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329113"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Zeit zu Einzelvorgängen in einer Stapelverarbeitung zuteilen

[!include [banner](../includes/banner.md)]

Sie können Einzelvorgänge in der Fertigungssteuerung bündeln. Sie können mehrere Einzelvorgänge auf der Seite "Einzelvorgangsliste" gleichzeitig starten.

Wenn Einzelvorgänge gebündelt werden, müssen Sie festlegen, wie die erfasste Gesamtzeit für alle Einzelvorgänge auf die einzelnen Einzelvorgänge verteilt werden soll. Sie definieren die Zuteilung, indem Sie eine der folgenden Optionen im Feld **Bündeltyp** auf der Seite **Verteilungsschlüssel** auswählen:

-   **Schätzung** – Die Zeit wird auf Basis der geschätzten Zeit für die Einzelvorgänge unter den Einzelvorgängen aufgeteilt.
-   **Einzelvorgänge** – Die Zeit wird entsprechend der Gesamtanzahl gebündelter Einzelvorgänge und der hierfür aufgewendeten gesamten Bearbeitungszeit aufgeteilt.
-   **Nettozeit** – Die Zeit wird gleichmäßig unter den jeweils im Bündel befindlichen Einzelvorgängen aufgeteilt.
-   **Echtzeit** – Die tatsächlich für den Einzelvorgang benötigte Zeit wird zugeteilt. Die Kosten können auf Basis der tatsächlichen Lohnkosten berechnet werden. **Hinweis:** Der Verteilungsschlüssel **Echtzeit** ist nur verfügbar, wenn Ihr Unternehmen die Lohnabrechnungsfunktionen in "Zeit und Anwesenheit" verwendet.

Die folgenden Ergebnisse zeigen die Ergebnisse der verschieden Verteilungsschlüssel.

## <a name="example-scenario"></a>Beispielszenario
Drei Einzelvorgänge in der Einzelvorgangswarteschlange müssen ausgefüllt werden. Sie starten den ersten Einzelvorgang, und dann, während dieser Einzelvorgang bearbeitet wird, starten Sie den zweiten und dritten Einzelvorgang. Daher gibt es ein Bündel von drei Einzelvorgängen. In der folgenden Tabelle wird die geschätzte Bearbeitungszeit für jeden Einzelvorgang dargestellt.

| Stelle   | Produktionszeit |
|-------|-----------------|
| Einzelvorgang 1 | 1 Stunde          |
| Einzelvorgang 2 | 3 Stunden         |
| Einzelvorgang 3 | 4 Stunden         |
| Summe | 8 Stunden         |

Die folgende Tabelle enthält die tatsächlichen Arbeitsstunden, die für jeden Einzelvorgang aufgewendet werden.

| Stelle    | Startzeit | Endzeit | Bündelzeit |
|--------|------------|----------|-------------|
| Einzelvorgang 1  | 09:00      | 11:00    | 2 Stunden     |
| Einzelvorgang 2  | 10:00      | 13:00    | 3 Stunden     |
| Einzelvorgang 3  | 10:00      | 15:00    | 5 Stunden     |
| Bündel | 09:00      | 15:00    | 6 Stunden     |

In den folgenden Abschnitten werden die Ergebnisse der berechneten Zeit für jeden Verteilungsschlüssel beschrieben.

## <a name="estimation-allocation-key"></a>Verteilungsschlüssel "Schätzung"
Die folgende Tabelle enthält die Formel zum Berechnen der zugewiesenen Zeit. Hier ist die Fomel: Zeit pro Einzelvorgang = Gesamte Bündelzeit × (Geschätzte Einzelvorgangszeit ÷ Gesamte geschätzte Zeit)

| Einzelvorgang   | Formel           | Zugeordnete Zeit |
|-------|-------------------|----------------|
| Einzelvorgang 1 | 6 × (1 ÷ 8) Stunden | 0,75 Stunden      |
| Einzelvorgang 2 | 6 × (3 ÷ 8) Stunden | 2,25 Stunden     |
| Einzelvorgang 3 | 6 × (4 ÷ 8) Stunden | 3,00 Stunden     |

## <a name="jobs-allocation-key"></a>Verteilungsschlüssel "Einzelvorgänge"
Die folgende Tabelle enthält die Formel zum Berechnen der zugewiesenen Zeit. Hier ist die Formel: Zeit pro Einzelvorgang = Gesamte Bündelzeit ÷ Anzahl der Einzelvorgänge

| Einzelvorgang   | Formel | Zugeordnete Zeit |
|-------|---------|----------------|
| Einzelvorgang 1 | 6 ÷ 3   | 2 Stunden        |
| Einzelvorgang 2 | 6 ÷ 3   | 2 Stunden        |
| Einzelvorgang 3 | 6 ÷ 3   | 2 Stunden        |

## <a name="net-time-allocation-key"></a>Zuweisungsschlüssel "Nettozeit"
Die folgende Tabelle enthält die Formel zum Berechnen der zugewiesenen Zeit. Hier ist die Formel: Berechnete Zeit pro Berichterstellung = Bündelzeit ÷ Anzahl der Einzelvorgänge

|                              | 09:00–10:00 (1 Stunde) | 10:00–11:00 (1 Stunde) | 11:00–13:00 (2 Stunden) | 13:00–15:00 (2 Stunden) | Zugeordnete Zeit |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Anzahl der Einzelvorgänge im Bündel | 1                    | 3                    | 2                     | 1                     | Nicht zutreffend |
| Einzelvorgang 1                        | 1 ÷ 1 = 1 Stunde       | 1 ÷ 3 = 0,33 Stunde    | Nicht zutreffend        | Nicht zutreffend        | 1,33 Stunden     |
| Einzelvorgang 2                        | Nicht zutreffend       | 1 ÷ 3 = 0,33 Stunde    | 2 ÷ 2 = 1 Stunde        | Nicht zutreffend        | 1,33 Stunden     |
| Einzelvorgang 3                        | Nicht zutreffend       | 1 ÷ 3 = 0,33 Stunde    | 2 ÷ 2 = 1 Stunde        | 2 ÷ 1 = 2 Stunden       | 3,33 Stunden     |

## <a name="real-time-allocation-key"></a>Verteilungsschlüssel "Echtzeit"
Wenn Produktionsaufträge auf Grundlage tatsächlicher Kosten kalkuliert werden sollen, müssen Sie die Option **Kostenkategorie** auf der Seite **Produktionsauftragsstandards** deaktivieren. Die folgende Tabelle enthält die Formel zum Berechnen der zugewiesenen Zeit. Hier ist die Formel: Tatsächliche Zeit pro Einzelvorgang = Tatsächliche Zeit im Bündel

| Einzelvorgang   | Tatsächliche Zeit |
|-------|-------------|
| Einzelvorgang 1 | 2 Stunden     |
| Einzelvorgang 2 | 3 Stunden     |
| Einzelvorgang 3 | 5 Stunden     |

Berücksichtigen Sie die drei Einzelvorgänge, die von einer Arbeitskraft ausgeführt werden, die einen Stundenlohn von 12,00 EUR hat. Für die für die Einzelvorgänge aufgewendete Zeit gibt es keine Überstundenzuschläge oder sonstige Zuschläge. Die Arbeitskraft hat für diese drei gebündelten Einzelvorgänge insgesamt sechs Stunden benötigt. Daher betragen die Lohnkosten 6 × 12,00 EUR = 72,00 EUR. Bei Verwendung der Zuteilung in Echtzeit werden die Kosten pro Stunde mit dem Faktor der Formel "Nettozeit" neu berechnet. Die tatsächlich für jeden Einzelvorgang aufgewendete Zeit wird nun zusammen mit dem korrigierten Stundeneinstandspreis übertragen. Im Beispiel wurden 6 Stunden aufgewendet, obwohl 10 Stunden zugeordnet wurden. Die folgende Tabelle enthält die Formel zum Berechnen der Kosten. Hier ist die Formel: Kosten pro Stunde = (Gesamte Bündelzeit pro Einzelvorgang (Nettozeit) ÷ Tatsächliche Zeit pro Einzelvorgang) × Standard-Einstandspreis pro Stunde

| Einzelvorgang   | Berechnung der korrigierten Kosten pro Stunde | Korrigierte Kosten pro Stunde | Zugeordnete Zeit | Gesamtkosten des Einzelvorgangs |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Einzelvorgang 1 | (1,33 ÷ 2) × 12,00 EUR                 | 8,00 EUR                | 2 Stunden        | 16,00 EUR         |
| Einzelvorgang 2 | (1,33 ÷ 3) × 12,00 EUR                 | 5,33 EUR                | 3 Stunden        | 16,00 EUR         |
| Einzelvorgang 3 | (3,33 ÷ 5) × 12,00 EUR                 | 8,00 EUR                | 5 Stunden        | 40,00 EUR         |

Die korrigierten Kosten pro Stunde und die Einzelvorgangszeit werden in einer Produktionserfassung gebucht. **Hinweis:** Wenn Sie die Option **Kostenkategorie** auf der Registerkarte **Allgemein** auf der Seite **Produktionsauftragsstandards** auswählen, wird die tatsächliche Zeit für jeden Einzelvorgang zu einer Produktionserfassung übertragen, wo die Kosten auf die Kostenkategorie des spezifischen Einzelvorgangs angewendet werden.



