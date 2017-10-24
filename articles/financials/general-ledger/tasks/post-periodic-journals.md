--- 
title: "Periodische Erfassungen veröffentlichen"
description: Periodische Erfassungen werden mitunter als wiederkehrende Erfassungen bezeichnet, da der Betrag, der Text und andere Informationen jedes Mal wiederholt werden, wenn die periodische Erfassung abgerufen wird.
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8eae11e0501db78e467e517b29a2bc19f5765e75
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="post-periodic-journals"></a>Periodische Erfassungen veröffentlichen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Periodische Erfassungen werden mitunter als wiederkehrende Erfassungen bezeichnet, da der Betrag, der Text und andere Informationen jedes Mal wiederholt werden, wenn die periodische Erfassung abgerufen wird. Wenn Sie die periodische Erfassung erstellen, geben Sie das Periodenintervall für die Wiederholung an, wie Tage oder Monate. Dieses Aufgabenhandbuch erstellt eine periodische Erfassung mit einer monatlichen Wiederholung.



1. Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Periodische Erfassungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Die Beschreibung ist der Name der "Periodischen Erfassung", wenn sie später abgerufen wird. Stellen Sie deshalb sicher, ihr einen entsprechenden Namen zu geben.  
6. Klicken Sie auf "Positionen".
    * Eine periodische Erfassung enthält normalerweise mehrere Erfassungspositionen. In diesem Aufgabenhandbuch wird jedoch nur eine Position hinzugefügt.  
7. Geben Sie ein Datum in das Feld "Datum" ein.
    * Das Feld "Datum" enthält das Buchungsdatum für die nächste Übertragung in die Tageserfassung. Für Erfassungen, die jeden Monat abgerufen werden, wird empfohlen, das Datum im Monat zu verwenden, in dem sie gebucht wird, normalerweise das erste oder letzte Datum der Periode. Es ist möglich, das Feld "Datum" leer zu lassen und ein Datum einzugeben, wenn die Erfassung abgerufen wird, und zwar mithilfe des Felds "Leerdatum".    Das Feld wird automatisch auf das nächste wiederkehrende Datum aktualisiert, an dem Buchungen abgerufen werden.  
8. Geben Sie im Feld "Konto" die gewünschten Werte an.
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Schließen Sie die Seite.
11. Geben Sie im Feld "Soll" eine Zahl ein.
12. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
13. Wählen Sie im Feld "Einheit" die Option "Monate" aus.
14. Geben Sie im Feld "Anzahl der Einheiten" den Wert "1" ein.
15. Geben Sie in das Feld "Letztes Datum" ein Datum ein.
    * Wenn Sie das letzte Datum in der vorhergehenden Periode eingeben, wird verhindert, dass die wiederkehrende Erfassung irrtümlicherweise im falschen Startzeitraum erstellt wird. Das letztes Datum wird später jedes Mal aktualisiert, wenn die periodische Erfassung abgerufen wird.  
16. Klicken Sie auf "Speichern".
17. Wechseln Sie zu "Standard-Dashboard".
18. Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".
19. Klicken Sie auf "Neu".
20. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
21. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
22. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
23. Geben Sie im Feld "Beschreibung" einen Wert ein.
24. Klicken Sie auf "Positionen".
25. Klicken Sie auf "Periodische Erfassung".
26. Klicken Sie auf "Erfassung abrufen".
27. Geben Sie in das Feld "Bis Datum" ein Datum ein.
    * Das "Bis Datum" dient als Abschnittsdatum für die periodischen Belegpositionen. Auf Grundlage der Wiederholungseinstellung werden das "Letzte Datum" und das "Bis Datum" in derselben Position möglicherweise mehr als einmal in die sich ergebende Erfassung einbezogen. Das "Bis Datum" wird automatisch auf Grundlage des Sitzungsdatums aktualisiert, an dem zum letzten Mal die periodische Position an eine Erfassung übertragen wurde.  
28. Geben Sie im Feld "Periodische Erfassungsnummer" einen Wert ein, oder wählen Sie einen Wert aus.
29. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
30. Klicken Sie auf "OK".
    * Die periodischen Erfassung kann je nach Bedarf und Einstellung jetzt überprüft, genehmigt oder gebucht werden.  


