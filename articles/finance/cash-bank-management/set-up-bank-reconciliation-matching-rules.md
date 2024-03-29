---
title: Abgleichsregeln für Bankabstimmung einrichten
description: Dieser Artikel erklärt, wie Sie Abstimmungsregeln und Abstimmungsregelsätze für den Bankabstimmungsprozess einrichten. Abstimmungsübereinstimmungsregeln sind eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Bankdokumentpositionen während des Abstimmungsvorgangs zu filtern.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803936"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Abgleichsregeln für Bankabstimmung einrichten

[!include [banner](../includes/banner.md)]

Dieser Artikel erklärt, wie Sie Abstimmungsregeln und Abstimmungsregelsätze für den Bankabstimmungsprozess einrichten. Abstimmungsübereinstimmungsregeln sind eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Bankdokumentpositionen während des Abstimmungsvorgangs zu filtern.

Sie können Abgleichsregeln für die Abstimmung und Abgleichsregelsatz für Bankabstimmung einrichten, um den Bankabstimmungsprozess zu unterstützen. Eine Abstimmungsübereinstimmungsregel ist eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Dynamics 365 Finance-Banktransaktionen während des Abstimmungsvorgangs zu filtern. Verwenden Sie die Seite **Abgleichsregeln für die Abstimmung**, um die Abgleichsregeln für die Abstimmung einzurichten. Sie können mehrere Abgleichsregeln einrichten und dann auf der Seite **Abgleichsregelsätze für die Abstimmung** eine Abgleichsregelsatz für Bankabstimmung erstellen. 

> [!NOTE] 
> Abgleichsregeln für Bankabstimmung werden verwendet, wenn Sie einen elektronischen Bankauszug mithilfe der Vorbankabstimmung abstimmen. 

Auf der Seite **Abgleichsregeln für die Abstimmung** können Sie auswählen, welche Aktivitäten und Auswahlkriterien verwendet werden, wenn die Abgleichsregel ausgeführt wird. Wählen Sie in der Gruppe **Aktionen** aus, welche Aktion ausgeführt wird, wenn die Übereinstimmungsregel während des Abstimmungsvorgangs ausgeführt wird.  

Standardmäßig stimmen Abgleichsregeln mit dem ersten Bankdokument überein, das die Kriterien für Abgleichsregeln erfüllt. Wenn mehrere Bankdokumente die Regelkriterien erfüllen, können Sie den Parameter aktivieren, für den ein manueller Abgleich erforderlich ist. Gehen Sie dafür zu **Bargeld- und Bankverwaltung > Setup > Bargeld- und Bankverwaltungsparameter > Bankabstimmung > Manueller Abgleich anfordern, wenn erweiterte Bankabstimmungs-Abgleichsregeln mehrere Dokumente finden, die mit dem Betrag übereinstimmen**.

> [!NOTE] 
> Die Option, mit der Sie auswählen, bestimmt die Felder, die angezeigt werden.

| Vorgang | Beschreibung   | Verfügbare Auswahlkriterien, wenn eine Aktivität aktiviert ist     |
|--------|---------------|----------------------------------------------------------|
| **Mit Bankdokument abgleichen**       | Erstellen Sie Kriterien, um anzugeben, wie die Bankdokumente und die Bankauszugspositionen abgeglichen werden, wenn die Abgleichsregel von der Seite **Bankabstimmungsarbeitsblatt** ausgeführt wird. Die Buchungspositionen werden entsprechend weiteren Kriterien ausgewählt, die auf den Inforegistern eingerichtet werden. | <ul><li>**Schritt 1: Definieren Sie die Abgleichsregel** – Wählen Sie die Kriterien aus, um anzugeben, welche Bankauszüge mit Finance-Banktransaktionen abgeglichen werden sollen.</li><li> **Schritt 2 (optional): Wählen Sie die Auszugspositionen aus, denen gegenüber Abgleichsregeln ausgeführt werden:**  Filtern Sie die Auszugsposition auf die die Regel angewendet wird.</li></ul>                                       |
| **Mehrere Auszugspositionen löschen** | Erstellen Sie Kriterien, um anzugeben, wie Rückbuchungsauszugspositionen von der Seite **Bankabstimmungsarbeitsblatt** entfernt werden sollen, wenn die Abgleichsregel ausgeführt wird. Diese Option wird verwendet, wenn wegen eines Bankfehlers zwei Bankauszugspositionen im importierten Bankauszug aufgeführt werden und die Positionen abgestimmt werden müssen. |<ul><li> **Schritt 1**: **Rückbuchungsauszugspositionen suchen** - Fügen Sie Auswahlkriterien hinzu, um Rückbuchungsauszugspositionen auszuwählen. Um beispielsweise nur Schecks auswählen, wählen Sie den **Bankbuchungscode** im Feld **Feld** aus, wählen Sie das Pluszeichen (+) im Feld **Operator** aus und geben Sie **Schecks** im Feld **Wert** ein. </li><li>**Schritt 2: Ursprüngliche Auszugspositionen suchen** - Sie können Auswahlkriterien hinzufügen, um zu Bankdokumentpositionen mit Bankauszugspositionen abzugleichen. </li><li>**Schritt 3: Finance-Bankbuchungen suchen** – Sie können Auswahlkriterien hinzufügen, um zu Finance-Banktrransaktionen mit Bankauszugspositionen abzugleichen.</li></ul>  |
| **Neue Buchungen markieren**          | Erstellen Sie Kriterien, um anzugeben, wie neue Transaktionen auf der Seite **Bankabstimmungsarbeitsblatt** markiert werden sollen, wenn die Abgleichsregel ausgeführt wird.                                                                                                                                                                 | <ul><li>**Schritt 1: Auszugspositionen suchen**- Fügen Sie Auswahlfelder hinzu, um anzugeben, welche Bankauszugspositionen auf der Seite **Bankabstimmungsarbeitsblatt** ausgewählt werden sollen.</li><li> **Schritt 2: Finanzen und Vorgänge finden** – Sie können Auswahlkriterien hinzufügen, um Zeilen mit Bankbelegen zu suchen. Wenn kein Bankdokument gefunden wird, wird eine Auszugsposition als neue Buchung markiert. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

