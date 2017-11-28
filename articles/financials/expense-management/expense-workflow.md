---
title: Spesenverwaltungsworkflow
description: "In diesem Thema wird erläutert, wie das Workflowsystem in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, verwenden können, um eines Prüfvorgangs für Spesenabrechnungen in der Spesenverwaltung zu verarbeiten."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a>Spesenverwaltungsworkflow

[!include[banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie das Workflowsystem in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, verwenden kann, um einen Prüfvorgang für Spesenabrechnungen in der Spesenverwaltung zu verarbeiten. Sie können einen Workflow einrichten, um zu bestimmen, wer Spesenabrechnungen unter den folgenden Kriterien genehmigt werden:

- Die Mitarbeiterunterstellungshierarchie und die vordefinierten Genehmigungslimits
- Genehmigung in mehreren Ebenen, die Zwischengenehmiger und einen letzten Genehmiger unterstützt
- Finanzdimensionen und Projektzuständigkeit
- Zuweisung zu bestimmten Benutzern oder Benutzergruppen

Workflowgenehmigungen können für Spesenabrechnungen, Reiseanforderungen, Barvorschüsse, Kreditkartenstreitigkeiten und Mehrwertsteuer (MwSt.)-Beitreibung erstellt werden.

**Beispiel**

Im Folgenden finden Sie ein Beispiel für einen Spesenverwaltungsworkflow für eine Spesenabrechnung:

1. Ein Mitarbeiter erstellt und speichert eine Spesenabrechnung.
2. Der Mitarbeiter übermittelt die Spesenabrechnung zur Genehmigung. Die genehmigende Person wird basierend auf den Regeln identifiziert, die definiert wurden, als der Standardworkflow eingerichtet wurde.
3. Die genehmigende Person wird benachrichtigt, dass eine zu genehmigende Spesenabrechnung vorliegt. Die genehmigende Person prüft die Spesenabrechnung und überprüft, dass die folgenden Bedingungen erfüllt sind:

    - Die Ausgaben verstoßen nicht gegen Ausgabenrichtlinien. Wenn Ausgaben eine Richtlinie verletzen, überprüft die genehmigende Person, dass eine gültiger Geschäftsbegründung im Bericht enthalten ist.
    - Der Spesenabrechnung sind elektronische Belege angefügt.

4. Die genehmigende Person genehmigt die Spesenabrechnung.
5. Die Spesenabrechnung wird dem Kreditorenkoordinator zur Buchung zugewiesen.
6. Einer der folgenden Schritte erfolgt, abhängig davon an, ob die automatische Buchung konfiguriert ist:

    - Wenn die automatische Buchungen konfiguriert ist, wird die Spesenabrechnung für die Zahlung verarbeitet, und der Status der Spesenabrechnung wird aktualisiert.
    - Wenn die automatische Buchung nicht konfiguriert ist, überprüft der Kreditorenkoordinator, dass alle ursprünglichen Zugänge gesendet wurden und dass die Zugänge den Ausgaben in der Spesenabrechnung entsprechen. Alle Steuercodes, die auf der Spesenabrechnung eingegeben werden, müssen ebenfalls auf Korrektheit geprüft werden.

Nachdem diese Anforderungen überprüft wurden, wird die Spesenabrechnung gebucht.

Nachdem die Spesenabrechnung gebucht wurde, wird die Zahlung für die Spesenabrechnung autorisiert und dem Mitarbeiter erstattet.

