---
title: Spesenverwaltungsworkflow
description: In diesem Thema wird erläutert, wie Sie das Workflowsystem in Microsoft Dynamics 365 for Finance and Operations verwenden können, um einen Prüfprozess für Spesenabrechnungen in der Spesenverwaltung einzurichten.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 037a6ae00b7d559f79860901f0cb2ad6ddddd7aa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "310115"
---
# <a name="expense-workflow"></a>Spesenverwaltungsworkflow

[!include [banner](../includes/banner.md)]

Mithilfe des Workflowsystems in Microsoft Dynamics 365 for Finance and Operations können Sie einen Prüfprozess für Spesenabrechnungen in "Ausgabenverwaltung" einrichten. Sie können einen Workflow einrichten, um zu bestimmen, wer Spesenabrechnungen unter den folgenden Kriterien genehmigt werden:

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
