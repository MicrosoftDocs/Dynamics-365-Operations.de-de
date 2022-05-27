---
title: Periodische Erfassungen veröffentlichen
description: Periodische Erfassungen werden mitunter als wiederkehrende Erfassungen bezeichnet, da der Betrag, der Text und andere Informationen jedes Mal wiederholt werden, wenn die periodische Erfassung abgerufen wird.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 412098c2027344bfc5309d814ee70d6ee98ca765
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716914"
---
# <a name="post-periodic-journals"></a>Periodische Erfassungen veröffentlichen

[!include [banner](../../includes/banner.md)]

Periodische Erfassungen werden mitunter als wiederkehrende Erfassungen bezeichnet, da der Betrag, der Text und andere Informationen jedes Mal wiederholt werden, wenn die periodische Erfassung abgerufen wird. Wenn Sie die periodische Erfassung erstellen, geben Sie das Periodenintervall für die Wiederholung an, wie Tage oder Monate. Dieses Aufgabenhandbuch erstellt eine periodische Erfassung mit einer monatlichen Wiederholung.

1. Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Periodische Aufgaben > Periodische Journale**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld **Beschreibung** einen Wert ein. Die Beschreibung ist der Name der "Periodischen Erfassung", wenn sie später abgerufen wird. Stellen Sie deshalb sicher, ihr einen entsprechenden Namen zu geben.
6. Klicken Sie im **Aktivitätsbereich** auf **Positionen**. Eine periodische Erfassung enthält normalerweise mehrere Erfassungspositionen. In diesem Aufgabenhandbuch wird jedoch nur eine Position hinzugefügt.
7. Geben Sie ein Datum in das Feld **Datum** ein. Das Feld **Datum** enthält das Buchungsdatum für die nächste Übertragung in die Tageserfassung. Für Erfassungen, die jeden Monat abgerufen werden, wird empfohlen, das Datum im Monat zu verwenden, in dem sie gebucht wird, normalerweise das erste oder letzte Datum der Periode. Es ist möglich, das Feld "Datum" leer zu lassen und ein Datum einzugeben, wenn die Erfassung abgerufen wird, und zwar mithilfe des Felds "Leerdatum". Das Feld wird automatisch auf das nächste wiederkehrende Datum aktualisiert, an dem Buchungen abgerufen werden. 
8. Geben Sie im Feld **Konto** die gewünschten Werte an.
9. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.
10. Schließen Sie die Seite.
11. Geben Sie im Feld **Soll** eine Zahl ein.
12. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
13. Wählen Sie im Feld **Einheit** die Option „Monate“ aus.
14. Geben Sie im Feld **Anzahl der Einheiten** den Wert „1“ ein.
15. Geben Sie in das Feld **Letztes Datum** ein Datum ein. Wenn Sie das letzte Datum in der vorhergehenden Periode eingeben, wird verhindert, dass die wiederkehrende Erfassung irrtümlicherweise im falschen Startzeitraum erstellt wird. Das letztes Datum wird später jedes Mal aktualisiert, wenn die periodische Erfassung abgerufen wird. 
16. Klicken Sie auf **Speichern**.
17. Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Journaleinträge > Allgemeine Erfassungen**.
18. Klicken Sie auf **Neu**.
19. Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.
20. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
21. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
22. Geben Sie im Feld **Beschreibung** einen Wert ein.
23. Klicken Sie im **Aktivitätsbereich** auf **Positionen**.
24. Klicken Sie im **Aktivitätsbereich** auf **Periodenjournal**.
25. Klicken Sie auf **Erfassung abrufen**.
26. Geben Sie im Feld **Bis Datum** ein Datum ein. Das **Bis Datum** dient als Abschnittsdatum für die periodischen Belegpositionen. Auf Grundlage der Wiederholungseinstellung werden das "Letzte Datum" und das "Bis Datum" in derselben Position möglicherweise mehr als einmal in die sich ergebende Erfassung einbezogen. Das "Bis Datum" wird automatisch auf Grundlage des Sitzungsdatums aktualisiert, an dem zum letzten Mal die periodische Position an eine Erfassung übertragen wurde. 
27. Geben Sie im Feld **Periodische Erfassungsnummer** einen Wert ein, oder wählen Sie einen Wert aus.
28. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
29. Klicken Sie auf **OK**. Die periodischen Erfassung kann je nach Bedarf und Einstellung jetzt überprüft, genehmigt oder gebucht werden.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
