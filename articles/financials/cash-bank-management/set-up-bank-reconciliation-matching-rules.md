---
title: "Einrichten von Abgleichsregeln für Bankabstimmung"
description: "Dieser Artikel erklärt, wie Sie Abstimmungsregeln und Abstimmungsregelsätze für den Bankabstimmungsprozess einrichten. Abstimmungsübereinstimmungsregeln sind eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Bankdokumentpositionen während des Abstimmungsvorgangs zu filtern."
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b48accdc7aaaa65b4c620777546b20056038905b
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Einrichten von Abgleichsregeln für Bankabstimmung

[!include[banner](../includes/banner.md)]


Dieser Artikel erklärt, wie Sie Abstimmungsregeln und Abstimmungsregelsätze für den Bankabstimmungsprozess einrichten. Abstimmungsübereinstimmungsregeln sind eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Bankdokumentpositionen während des Abstimmungsvorgangs zu filtern.

Sie können Abgleichsregeln für die Abstimmung und Abgleichsregelsatz für Bankabstimmung einrichten, um den Bankabstimmungsprozess zu unterstützen. Eine Abstimmmungsregel ist eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Microsoft Dynamics 365 for Finance and Operations  Banktransaktionspositionen während des Abstimmungsvorgangs zu filtern. Verwenden Sie die Seite **Abgleichsregeln für die Abstimmung**, um die Abgleichsregeln für die Abstimmung einzurichten. Sie können mehrere Abgleichsregeln einrichten und dann auf der Seite **Abgleichsregelsätze für die Abstimmung** eine Abgleichsregelsatz für Bankabstimmung erstellen. 

> [!NOTE] 
> Abgleichsregeln für Bankabstimmung werden verwendet, wenn Sie einen elektronischen Bankauszug mithilfe der Vorbankabstimmung abstimmen. 

Auf der Seite **Abgleichsregeln für die Abstimmung** können Sie auswählen, welche Aktivitäten und Auswahlkriterien verwendet werden, wenn die Abgleichsregel ausgeführt wird. Wählen Sie in der Gruppe **Aktionen** aus, welche Aktion ausgeführt wird, wenn die Übereinstimmungsregel während des Abstimmungsvorgangs ausgeführt wird.  

> [!NOTE] 
> Die Option, mit der Sie auswählen, bestimmt die Felder, die angezeigt werden.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktion**                         |                                                                                                                                                                                                                                                                                                               | **Verfügbare Auswahlkriterien, wenn eine Aktivität aktiviert ist**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Mit Bankdokument abgleichen**       | Erstellen Sie Kriterien, um anzugeben, wie die Bankdokumente und die Bankauszugspositionen abgeglichen werden, wenn die Abgleichsregel von der Seite **Bankabstimmungsarbeitsblatt** ausgeführt wird. Die Buchungspositionen werden entsprechend weiteren Kriterien ausgewählt, die auf den Inforegistern eingerichtet werden.                                | **Schritt 1: Definieren Sie die Abgleichsregel** – Wählen Sie die Kriterien aus, um anzugeben, welche Bankauszüge mit Finance and Operations Banktransaktionen abgeglichen werden sollen. **Schritt 2 (optional): Wählen Sie die Auszugspositionen aus, denen gegenüber Abgleichsregeln ausgeführt werden:**  Filtern Sie die Auszugsposition auf die die Regel angewendet wird.                                                                                                                                                                                                                                                                                                               |
| **Mehrere Auszugspositionen löschen** | Erstellen Sie Kriterien, um anzugeben, wie Rückbuchungsauszugspositionen von der Seite **Bankabstimmungsarbeitsblatt** entfernt werden sollen, wenn die Abgleichsregel ausgeführt wird. Diese Option wird verwendet, wenn wegen eines Bankfehlers zwei Bankauszugspositionen im importierten Bankauszug aufgeführt werden und die Positionen abgestimmt werden müssen. | **Schritt 1**:**Rückbuchungsauszugspositionen suchen** - Fügen Sie Auswahlkriterien hinzu, um Rückbuchungsauszugspositionen auszuwählen. Um beispielsweise nur Schecks auswählen, wählen Sie den **Banktransaktionscode** im "Feld"-Feld aus, wählen das Pluszeichen (+) (+) im Feld **Operator** aus und geben **Schecks** im Wertfeld ein. **Schritt 2: Ursprüngliche Auszugspositionen suchen** - Sie können Auswahlkriterien hinzufügen, um zu Bankdokumentpositionen mit Bankauszugspositionen abzugleichen. **Schritt 3: Dynamics 365 for Finance and Operations-Bankbuchungen suchen** – Sie können Auswahlkriterien hinzufügen, um zu Dynamics 365 for Finance and Operations-Banktrransaktionen mit Bankauszugspositionen abzugleichen. |
| **Neue Buchungen markieren**          | Erstellen Sie Kriterien, um anzugeben, wie neue Transaktionen auf der Seite **Bankabstimmungsarbeitsblatt** markiert werden sollen, wenn die Abgleichsregel ausgeführt wird.                                                                                                                                                                 | **Schritt 1: Auszugspositionen suchen**- Fügen Sie Auswahlfelder hinzu, um anzugeben, welche Bankauszugspositionen auf der Seite **Bankabstimmungsarbeitsblatt** ausgewählt werden sollen. **Schritt 2: Finance and Operations** – Sie können Auswahlkriterien hinzufügen, um Bankdokumentpositionen zu suchen. Wenn kein Bankdokument gefunden wird, wird eine Auszugsposition als neue Buchung markiert.                                                                                                                                                                                                                                             |

 







