---
title: SEPA-Direkteinzugsmandate einrichten
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


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

Siehe auch [Direktbelastungsüberblick](sepa-direct-debit-overview.md) 



