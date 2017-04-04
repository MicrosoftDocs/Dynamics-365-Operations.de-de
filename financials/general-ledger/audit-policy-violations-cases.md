---
title: "Überwachungsrichtlinienverletzungen und -anfragen"
description: "Der Artikel beschrieben, wie Überwachungsanfragen aus den Verletzungen von Überwachungsrichtlinienregeln generiert werden. Er umfasst außerdem Informationen zu den verschiedenen Methoden, die Überwachungsrichtlinien für den Datumsbereich für die Dokumentauswahl verwenden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 77f72c9414f1fad720055e58e3f704b9c713072f
ms.lasthandoff: 03/31/2017


---

# <a name="audit-policy-violations-and-cases"></a>Überwachungsrichtlinienverletzungen und -anfragen

Der Artikel beschrieben, wie Überwachungsanfragen aus den Verletzungen von Überwachungsrichtlinienregeln generiert werden. Er umfasst außerdem Informationen zu den verschiedenen Methoden, die Überwachungsrichtlinien für den Datumsbereich für die Dokumentauswahl verwenden.

<a name="how-audit-cases-are-generated"></a>Generieren von Überwachungsanfragen
-----------------------------

Mithilfe von Überwachungsrichtlinien werden Spesenabrechnungen, Bestellungen und Kreditorenrechnungen ermittelt, die den von Ihnen als Überwachungsrichtlinienregeln definierten und konfigurierten Geschäftsregeln widersprechen. 

Überwachungsrichtlinien werden im Stapelverarbeitungsmodus ausgeführt. Wenn Sie eine Überwachungsrichtlinie ausführen, werden alle Regeln der Richtlinie gleichzeitig ausgeführt.

Jede Richtlinienregel wertet eine Reihe von Dokumenten aus. Die Richtlinienregel wählt die Dokumente aus, die sich im Datumsbereich für die Dokumentauswahl befinden und den angegebenen Kriterien entsprechen. Mit einer Richtlinienregel können z. B. Spesenabrechnungen ausgewählt werden, die Mahlzeiten für über 50,00 EUR enthalten. Mit einer anderen Richtlinienregel können Kreditorenrechnungen ausgewählt werden, die an einen bestimmten Kreditor zu zahlen sind. Für jedes Dokument, das in der Gruppe ausgewählt wird, wird ein Verstoß generiert. Bei diesem Verstoß wird in einem Datensatz aufgezeichnet, dass ein bestimmtes Dokument (z. B. Rechnung 12345) der Richtlinienregel nicht entspricht. 

Dabei werden mehrere Datensätze für Überwachungsverstöße gruppiert und Überwachungsanfragen zugeordnet. Anfragen für die einzelnen Überwachungsrichtlinien werden standardmäßig nach der Überwachungsrichtlinienregel gruppiert. Wenn Sie es bevorzugen, können Sie andere Gruppierungskriterien auswählen, indem Sie die Seite **Anfragegruppierungskriterien** verwenden. So können Sie Ausgabenenköpfe nach Projektkennung und Kreditorenrechnungen nach Kreditorenkonto gruppieren. In diesem Fall werden alle Ausgabenenkopfverstöße, die dieselbe Projektkennung haben, in derselben Anfrage und allen Kreditorenrechnungen, die mit demselben Kreditorenkonto aufweisen, gruppiert werden in derselben Anfrage gruppiert. 

> [!NOTE]
> Bei Überwachungsrichtlinienregeln, die auf Grundlage eine sind ** Duplikat ** Abfragetyp, werden Verstöße nicht nach Richtlinienregel oder nach den Kriterien gruppiert, die der auf ** Anfragegruppierungskriterien ** Seite angegeben werden. Die Gruppierung richtet sich stattdessen nach den in die Überwachungsrichtlinienregel integrierten Kriterien. Wenn beispielsweise eine Richtlinienregel Spesenrechnungen auf doppelte Ausgaben auswertet, bei denen Betrag, Händlerkennung und Datum übereinstimmen, stellen alle Ausgaben mit denselben Werten in diesen Feldern eine Anfrage dar. Alle Ausgaben, die verschiedene Werte besitzen, sind getrennte Anfragen.

Nachdem die Überwachungsanfragen generiert wurden, werden sie mit den üblichen Prozessen der Anfrageverwaltung verarbeitet.

## <a name="document-selection-date-ranges"></a>Datumsbereich für die Dokumentauswahl
Beim Ausführen einer Überwachungsrichtlinie wählt jede Richtlinienregel Dokumente vom angegebenen Typ aus, die ein Datum aus dem Datumsbereich für die Dokumentauswahl aufweisen. Der Datumsbereich für die Dokumentauswahl wird auf der Seite **Zusätzliche Optionen** festgelegt. Vielen Dokumenten sind mehrere Datumsangaben zugeordnet. Das Datumsfeld, das der Überwachungsrichtlinienregel verwendet, wird auf der Seite **Richtlinienregeltyp** angegeben.

Nachfolgend werden einige andere Methoden aufgeführt, auf die eine Überwachungsrichtlinie den Datumsbereich für die Dokumentauswahl verwendet:

-   In der Richtlinie wird die Version jeder Richtlinienregel verwendet, die am letzten Tag des Datumsbereichs für die Dokumentauswahl gültig ist. Sie können die Gültigkeitsdaten der einzelnen Richtlinienregeln auf der Listenseite **Überwachungsrichtlinien** anzeigen.
-   In der Richtlinie werden die Organisationsknoten verwendet, die der Richtlinie am letzten Tag des Datumsbereichs für die Dokumentauswahl zugeordnet sind. Auf der Listenseite **Überwachungsrichtlinien** werden nur die Organisationsknoten angezeigt, die der Richtlinie gegenwärtig zugeordnet sind.
-   Für auf dem Abfragetyp **Listensuche** basierende Richtlinienregeln wertet die Richtlinie Dokumente für überwachte Entitäten aus, die am letzten Tag des Datumsbereichs für die Dokumentauswahl gültig sind.


Weitere Informationen finden Sie audit-policy-rules.md Überwachungsrichtlinienregeln [] ()


