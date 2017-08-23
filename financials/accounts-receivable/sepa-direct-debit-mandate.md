---
title: SEPA-Direkteinzugsmandate einrichten
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 17dc0cc19c4c58e6c795e085e2e8985598d403a0
ms.openlocfilehash: 4ea72cf6410eb30d83103bceb4a1628bafd33ac7
ms.contentlocale: de-de
ms.lasthandoff: 08/09/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA-Direkteinzugsmandate einrichten

[!include[banner](../includes/banner.md)]




Eine SEPA-Direktbelastung ermöglicht einem Kreditgeber Mittel vom Bankkonto eines Debitors einzuziehen, vorausgesetzt, dass eine signierte Einzugsermächtigung dem Kreditor vom Debitor gewährt wurde. Der Debitor signiert eine Einzugsermächtigung, die den Lieferanten autorisiert, eine Zahlung einzuziehen und die Bank des Debitors anweist, die Sammlung zu bezahlen. In diesem Thema wird erläutert, um den Prozess zum Einrichten von SEPA-Direktbelastungsvollmachten anzuzeigen.

## <a name="prerequisites"></a>Voraussetzungen
In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.

| Kategorie       | Voraussetzung                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/Region | Die Hauptadresse für die juristische Person muss in den folgenden Ländern/Regionen sein: Österreich, Deutschland, Spanien, Frankreich, Italien, oder die Niederlande. |

1. Einrichten eines Nummernkreises für Direktbelastungsvollmachten, die jede Direktbelastungsvollmacht eine eindeutige Zahl besitzen muss. Verwenden Sie die Seite **Nummernkreis**, um einen Nummernkreis für Direktbelastungseinzugsermächtigungen zu erstellen. Sie verwenden diese Kennung, um den Nummernkreis dem Direktbelastungseinzugsermächtigungssystem im Formular **Debitorenkontenparameter** zuzuweisen.

2. Einrichten von Debitorenparametern für Direktbelastungsvollmachten verwenden die **Debitorenparameter** Seite, um Parameter für Direktbelastungsvollmachten einzurichten. Die Parameter, auf der Registerkarte einrichten **Direktbelastung** Änderung die Standardparameter, wie Sie benötigen. Stellen Sie anschließend auf der Registerkarte **Nummernkreise** aktualisieren Sie das **Direktbelastungsvollmacht-Kennung** Feld dem Sie vor diesem Nummernkreis einrichten.

3. Einrichten einer Zahlungsmethode für Direktbelastungseinzugs-ermächtigungen. Um eine Zahlungsmethode für Direktbelastungseinzugsermächtigungen einzurichten, müssen Sie diese zusätzlichen Schritte für eine Zahlungsmethode durchführen: Sie verwenden diese Zahlungsmethode, um Rechnungen abfragen, die das Abbuchen generieren. Verwenden Sie die Seite **Zahlungsmethoden**, um die Zahlungsmethode einzurichten. Um eine Zahlungsmethode für Direktbelastungseinzugsermächtigungen einzurichten, müssen Sie diese zusätzlichen Schritte für eine Zahlungsmethode durchführen:

-   Wählen Sie im Feld **Zahlungstyp** **Elektronischer Zahlungsverkehr** aus.
-   Optional: Wenn Sie von jedem Ihrer Debitoren erwarten, mehrere Einzugsermächtigungen zu haben, wählen Sie im Feld **Zeitraum** **Rechnung** aus. Dieses erstellt eine separate Zahlung für jede Rechnung, und jede Zahlung verwendet die Einzugsermächtigung, die für die Rechnung angegeben ist.
-   Wählen Sie die **Mandat anfordern**-Option aus, um Zahlungen zu erstellen, indem Sie Direktbelastungseinzugsermächtigungen verwenden. Die **Mandat anfordern**-Option ist nur verfügbar, wenn Sie **Elektronischer Zahlungsverkehr** im Feld **Zahlungstyp** auswählen.

Siehe auch

[Direktbelastungsüberblick](sepa-direct-debit-overview.md) 

[Direkteinzugsmandat für einen Debitor erstellen](tasks/create-direct-debit-mandate-customer.md) 


