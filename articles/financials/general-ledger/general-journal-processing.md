---
title: Allgemeine Erfassungsverarbeitung
description: "Dieser Artikel beschreibt die Funktionen in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edtion, mit denen die allgemeine Erfassung einfacher wird, und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die internen Kontrollen nicht beeinträchtigt werden."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 68da281cb4793ed83f70c68d061d327aa8a8c772
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="general-journal-processing"></a>Allgemeine Erfassungsverarbeitung

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt die Funktionen in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edtion, mit denen die allgemeine Erfassung einfacher wird, und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die internen Kontrollen nicht beeinträchtigt werden.  

Journale

Einer der wichtigsten Bereiche einrichten ist Journale. Es empfiehlt sich, bestimmte Journale für jeden Zweck, wie Abgrenzungsregulierung Fehlerkorrektur Intercompany, und zu definieren. Sie können jedes Journal anpassen, mit deren Hilfe, Dateneingabe für jeden Zweck einfach und sicherstellen zu machen. 

Auf der Seite **Journale** können Sie folgende Elemente einrichten:

-   **Workflowgenehmigung** - Definieren Sie Journal-Workflows, die basierend auf Kriterien wie „Gesamt“ oder „Betrag“ Wesentlichkeitsgrenzen für Überprüfung- und Genehmigungsschritte festlegen, um die interne Kontrolle zu erhöhen. Sie richten Workflows für die allgemeinen Erfassungen auf der Seite **Hauptbuchworkflows** ein.
-   **Standardwerte** – Wählen Sie Standardwerte für Gegenkonten, Währung und Finanzdimensionen aus.
-   **Erfassungssteuerung** – Richten Sie Einschränkungen für den Unternehmens- und Kontotyp und die Segmentwerte ein. 

**Beispiele**

Ein Journal kann nur für Regulierungen verwendet werden. In diesem Fall können Sie angeben, dass nur die **Sachkonto**-Kontenart für alle Unternehmen gültig ist. [![Erfassungssteuerungs-Kontotypen](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Ein Journal kann nur für ein bestimmtes Segment oder für einen Bereich für Hauptkonten verwendet werden. [![Erfassungssteuerungssegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Die Option **Automatische Rückbuchung** ist nur in allgemeinen Erfassungen verfügbar. Beispiel: Sie haben eine Abgrenzungsregulierung, in der das eigentliche Dokument noch nicht verarbeitet wurde, wie in der folgenden Abbildung dargestellt.
[![Erfassungsrücksetzung](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Rückbuchung allgemeine Erfassung Das Microsoft Excel-Add-in für Journaleinträge bietet eine weitere Ebene der Automatisierung und erleichtert die Dateneingabe. Die **Positionen in Excel öffnen**-Aktivität ist auf den Seiten **Allgemeine Erfassung** und **Alle Journale** verfügbar. 

Auf der Seite **Periodische Erfassungen** können Sie wiederholende Erfassungen einrichten, um die Erfassungsverarbeitung zu automatisieren. 

Belegvorlagen können jederzeit verwenden. Auf der Seite **Allgemeine Erfassungen** finden Sie die Aktivitäten **Speichern** und **Belegvorlage auswählen** auf der Seite **Alle Journale** unter **Funktionen**.

## <a name="related-setup"></a>Verwandte Einstellung
Die folgende Einstellung ist für allgemeine Erfassungen nicht spezifisch, sorgt aber dafür, dass die Dateneingabe richtig und einfach ist.

### <a name="main-account"></a>Hauptkonto

Die Hauptkontoeinstellung stellt viele Optionen zum Verarbeiten der allgemeinen Erfassung bereit:

-   **SOLL/HABEN-Anforderung** - Verwenden Sie diese Option, wenn ein Hauptkonto auf Soll- oder Habenbuchungen beschränkt ist. Die Einstellung wird überprüft, wenn eine Erfassung geprüft oder gebucht wird.
-   **Standardgegenkonto**
-   **Unterbrochen** – Aussetzen eines Hauptkontos für die Dateneingabe für alle Unternehmen oder für ein bestimmtes Unternehmen bzw. bestimmte juristische Personen
-   **Keine manuellen Eingaben zulassen** – Verhindert, dass Benutzer in Erfassungen manuell einen Wert für dieses Konto eingeben
-   **Standard-Währung/Währung prüfen**
-   **Juristische Person überschreibt** - Diese Einstellung ist spezifisch für das definierte Unternehmen/die definierte juristische Person:
    -   **Standard-MwSt/MwSt prüfen**
    -   **Standarddimension** – **Nicht fixiert** oder **Fester Wert** **Fester Wert** unterstützt, dass alle Buchungen für dieses Hauptkonto immer einen beliebigen Dimensionswert verwenden, der als **Fest** eingerichtet ist.
-   **Buchungsprüfung**
    -   **Benutzervalidierung** - Diese Option regelt, welche Benutzer auf ein Hauptkonto buchen dürfen.
    -   **Überprüfung des Buchungstyps** – Diese Option regelt, welche Buchungsarten für ein Hauptkonto zulässig sind.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Buchhaltungsstrukturen und Strukturen für erweiterte Regeln

Buchhaltungsstrukturen und Strukturen für erweiterte Regeln sind sehr wichtig, um sicherzustellen, dass die Daten, die für die Finanzberichterstellung und die Leistungsnachverfolgung erforderlich sind, während der allgemeinen Erfassungsverarbeitung und in allen Dokumentationen erfasst werden. Mit Buchhaltungsstrukturen und Strukturen für erweiterten Regeln können Sie die Dateneingabeerfahrung anpassen. Sie können die Dateneingabe nur für Finanzdimensionen zulassen, die in jeder Situation relevant sind. Sie können auch die Anforderung erzwingen, dass erforderliche und korrekte Daten immer erfasst werden.

Weitere Informationen finden Sie in folgenden Themen:
- [Kontenplan planen](plan-chart-of-accounts.md). 
- [Erweiterte Regeln für Erfassungen erstellen](tasks/create-advanced-rules-journals.md)
- [Journaleinträge mithilfe einer Vorlage erstellen](tasks/create-journal-entry-template.md)
- [Erfassungen erstellen und validieren](tasks/create-validate-journals.md)
- [Periodische Erfassungen veröffentlichen](tasks/post-periodic-journals.md)
- [Sachkonto-Zuordnungserfassung verarbeiten](tasks/process-ledger-allocation-journal.md)



