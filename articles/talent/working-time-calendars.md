---
title: Arbeitszeitkalender
description: In diesem Thema wird das Arbeiten mit Arbeitszeitkalendern in Dynamics 365 Talent – Core HR wie auch das Einrichten von Kalendern beschrieben.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: f69bfec663cb8473c112f108813f042368439570
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897234"
---
# <a name="working-time-calendars"></a>Arbeitszeitkalender

Mit dem Arbeitszeitkalender können Sie einen Kalender mit den Stunden erstellen und Tagen erstellen, die ein Mitarbeiter in Ihrer Organisation arbeitet. Kalender optimieren den Freizeitanforderungsprozess standardmäßig in Stunden oder in Tagen. Wenn ein Mitarbeiter eine Freizeitanforderung übermittelt, müssen sie sich jedoch nicht um Feiertage und Schließungen sorgen, da dies für sie im Arbeitszeitkalender bearbeitet wird.

## <a name="setting-up-a-working-time-calendar"></a>Arbeitszeitkalender einrichten

Kalender umfassen Generierungsdetails, die Tage und die Stunden, die Sie einschließen möchten, die Tage des Kalenders, Arbeitszeiten für die einzelnen Tage sowie erfasste Mitarbeiter. 

Um einen Kalender einzurichten, gehen Sie folgendermaßen vor:

1. Klicken Sie auf der Seite **Organisationsadministration** auf **Kalender**.

2. Klicken Sie im Aktivitätsbereich und wählen Sie **Neu** aus und geben Sie einen Namen und eine Beschreibung ein.

3. Wählen Sie die Arbeitstage für Ihre Organisation aus und geben Sie Arbeitszeit ein.

4. Fügen Sie Feiertagen und Schließungen hinzu, indem Sie die Schaltfläche **Hinzufügen** verwenden.

5. Geben Sie den Namen und die Beschreibung für die Schließungen und Feiertage ein, wie US-Feiertage oder gesetzliche Feiertage. Geben Sie die Daten für Urlaube und Schließungen ein. Speichern Sie die Urlaubszeiten und die Schließungsliste und schließen Sie die Seite.

6. Wählen Sie die Nummer und die Schließungsliste im Dropdownmenü aus.

7. Wenn die Mitarbeiter Nichtarbeitszeit haben, wie z. B. Mittagessen oder Pausen, legen Sie diese ebenfalls fest. Wählen Sie **Nicht-Arbeitszeit** aus und geben Sie den Namen und den Zeitraum ein. Schließen Sie die Seite. 

8. Klicken Sie **Hinzufügen**, um die Nichtarbeitszeit dem Kalender hinzufügen.

9. Auf der Registerkarte **Tage** wählen Sie **Generieren**, um die Tage in dem Kalender zu generieren. Geben Sie den Datumsbereich für den Kalender ein. Die Tage und die Arbeitszeiten werden auf Grundlage der Arbeitstage und - zeiten generiert, die unter den Generierungsoptionen in Kombination mit den ausgewählten Daten festgelegt werden.

10. Um einen Kalender Mitarbeitern zuzuweisen, wählen Sie **Mitarbeiter zuweisen** im Aktivitätsbereich aus. Wählen Sie die Mitarbeiter, die Sie diesem Kalender zuweisen möchten, und klicken Sie dann auf **Zuweisen**.

Mitarbeiter müssen keine zugewiesenen Kalender haben. Wenn es einen definierten Arbeitszeitkalenders gibt, werden Freitage automatisch aus der Anforderung ausgeschlossen. Der Betrag, in Stunden oder Tagen, entspricht standardmäßig den Arbeitszeiten, die im Kalender definiert sind. Wenn ein Mitarbeiter keinen zugeordneten Kalender hat, sind alle Tage für Freizeit verfügbar und die Dauer der Freizeit ist kein Standardwert für die Anforderung. 
