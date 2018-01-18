---
title: SEPA-Direkteinzugsvollmacht einrichten
description: "Eine SEPA-Direktbelastung ermöglicht einem Kreditgeber Mittel vom Bankkonto eines Debitors einzuziehen, vorausgesetzt, dass eine signierte Einzugsermächtigung dem Kreditor vom Debitor gewährt wurde."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5b9afeb24692010ca5de33156f372d86f167161e
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA-Direkteinzugsvollmacht einrichten

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


