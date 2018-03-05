---
title: "Arbeitsbereich für die Bankverwaltung"
description: "Dieses Thema enthält Informationen zum Bankwesen-Arbeitsbereich. Der Arbeitsbereich zeigt Informationen hinsichtlich der Bankkonten des Unternehmens und enthält eine Zusammenfassungsansicht und eine Analyseseite. Die Zusammenfassungsansicht zeigt Übersichtskacheln, Bankkontoinformationen, ein Saldodiagramm und zugehörige Informationen an. Die Analyseseite verwendet die Funktionen von Microsoft Power BI, um grafische Elemente hinsichtlich der Bankkontosalden anzuzeigen."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5d9f9aab56441a7ecd2407b5571de77ece2ab3f
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---
# <a name="bank-management-workspace"></a>Arbeitsbereich für die Bankverwaltung

[!include[banner](../includes/banner.md)]

Der Arbeitsbereich **Bankwesen** zeigt Informationen bezüglich der Bankkonten des Unternehmens. Der Arbeitsbereich umfasst eine Ansicht **Zusammenfassung** und eine Seite **Analyse**. Die **Zusammenfassungsansicht** zeigt Übersichtskacheln, Bankkontoinformationen, ein Saldodiagramm und zugehörige Informationen an. Die **Analyseseite** verwendet die Funktionen von Microsoft Power BI, um grafische Elemente hinsichtlich der Bankkontosalden anzuzeigen.

## <a name="summary-view"></a>Zusammenfassungsansicht

### <a name="summary"></a>Summe

Die Kacheln im Abschnitt **Zusammenfassung** bieten einen Überblick der Bankkonten und schnellen Zugriff auf Seiten, die Sie am häufigsten verwenden müssen. Die Bankabstimmungsinformationen sind für die erweiterten Bankabstimmungsfunktionen spezifisch. Informationen sind nur für die Bankkonten enthalten, bei denen die Option **Erweiterte Bankabstimmung** auf **Ja** auf der Seite **Bankkonto** festgelegt ist. Im Abschnitt **Zusammenfassung** können Sie elektronische Bankdateien für Bankkonten für alle juristischen Person importieren.

### <a name="bank-accounts"></a>Bankkonten

Jedes Bankkonto bei der juristischen Person wird als eine Karte im Abschnitt **Bankkonten** angezeigt. Der aktuelle Saldo wird angezeigt und Sie können Detailinformationen zu den Buchungen anzeigen, aus denen dieser zusammengefasste Saldobetrag besteht. Für den Betrag **Transferbuchungen** können Sie auch Detailinformationen zu den Buchungen anzeigen, aus denen dieser zusammengefasste Betrag besteht. Transferbuchungen sind alle ausstehende Buchungen, die bereits mithilfe der Transferfunktionen ausgeführt wurden, aber noch nicht verrechnet wurden. Der Betrag **Ausstehender Saldo** ist der aktuelle Saldos minus der Transfer- oder ausstehenden Buchungen.

Die Karte zeigt außerdem an, wann das Bankkonto zuletzt abgestimmt wurde. Diese Informationen werden nur angezeigt, wenn die erweiterte Bankabstimmung für das Bankkonto aktiviert ist.

### <a name="balance"></a>Bilanz

Das **Saldo**-Diagramm zeigt historische Saldoinformationen für das Bankkonto an, das im **Bankkonten**-Abschnitt ausgewählt wurde, oder eine Übersicht der historischen Saldoinformationen für alle Bankkonten bei der juristischen Person. Diese Informationen sind für verschiedene Zeiträume verfügbar: die aktuelle Woche, den aktuellen Monat, das aktuelle Jahr, die letzten fünf Jahre und alle Zeiträume (der vollständige Verlauf des Bankkontos). 

Wenn Sie das **Saldo**-Diagramm für ein einzelnes Bankkonto anzeigen, werden die historischen Salden in der Bankkontowährung angezeigt. Wenn Sie das Saldo-Diagramm aller Bankkonten der juristischen Person anzeigen, werden die historischen Salden in der Buchhaltungswährung angezeigt.

Informationen dazu, wann die Daten zuletzt aktualisiert wurden, werden am Anfang des Diagramms angezeigt. Sie können die Daten bei Bedarf aktualisieren.

### <a name="related-information"></a>Zugehörige Informationen

Aus dem Abschnitt **Zugehörige Informationen** können Sie die Seite **Allgemeine Erfassung** öffnen, um Banküberweisungen abzuschließen. Sie können die Seiten **Bankbuchungen** und **Transferbuchungen** auch schnell öffnen.

## <a name="analytics-view"></a>Analyseansicht

Die Seite **Analyse** enthält wichtige Metriken zu Bankkonten im aktuellen Unternehmen. Die folgenden Visualisierungen sind auf der Seite verfügbar:

-   Gesamter Banksaldo in der Systemwährung
-   Saldo nach juristischer Person
-   Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung
-   Saldo nach Bankkonto
-   Saldo in Währung

Sie können die Bankanalyse für alle Unternehmen im Arbeitsbereich **Bargeldüberblick – alle Unternehmen** anzeigen.

