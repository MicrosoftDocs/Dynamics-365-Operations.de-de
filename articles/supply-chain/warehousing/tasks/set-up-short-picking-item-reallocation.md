---
title: Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten
description: In diesem Verfahren erfahren Sie, wie Sie Lagerarbeiter ermöglichen alternative Lagerplätze schnell zu finden wenn kein ausreichender Bestand am Lagerort vorhanden ist.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf56a0811c4793ee2e3eaf78c8696c3c29e984c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560836"
---
# <a name="set-up-short-picking-item-reallocation"></a>Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Verfahren erfahren Sie, wie Sie Lagerarbeiter ermöglichen alternative Lagerplätze schnell zu finden wenn kein ausreichender Bestand am Lagerort vorhanden ist. Es ist möglich einen automatischen Neuzuordnungsprozess zu verwenden, der Lagerplatzrichtlinien verwendet, um Waren zu erhalten, wenn sie an einem anderen Standort verfügbar sind. Alternativ wird bei der manuellen Neuzuordnung eine Liste der Lagerplätze mit der verfügbaren Menge im mobilen Gerät angezeigt und ermöglicht dem Lagerarbeiter auszuwählen welcher Lagerplatz verwendet werden soll. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="set-up-work-exceptions"></a>Arbeitsausnahmen einrichten
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsausnahmen".
2. Klicken Sie auf "Neu".
    * Es ist möglich, dass mehrere Arbeitsausnahmen mit unterschiedlichen Artikelneuzuordnungsrichtlinien zu definieren, um den Lagerarbeitern die Auswahl basierend auf den Anforderungen der Lieferung zu ermöglichen, die diese verarbeitet.  
3. Geben Sie im Feld "Arbeitsausnahmecode" einen Wert ein.
    * Geben Sie der Arbeitsausnahme einen Titel, um anzugeben, für was sie verwendet wurde. Beispiel: "Manuelle Entnahme".  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Ausnahmetyp" "Entnahme mit unzureichender Menge" aus.
6. Aktivieren Sie das Kontrollkästchen Bestandsregulierung.
    * Diese Option bedeutet, dass der Lagerbestand am Entnahmelagerplatz automatisch auf 0 angepasst wird.  
7. Geben Sie im Feld "Standardmäßiger Regulierungstypcode" einen Wert ein oder wählen Sie einen Wert aus.
    * In USMF können Sie beispielsweise 'Remove Res Adj Out' auswählen.  
8. Wählen Sie im Feld "Artikelneuzuteilung" 'Manuell' aus.
    * Wenn Sie "Manuell" oder "Automatisch und manuell" auswählen, muss der Lagerarbeiter für die manuelle Neuzuordnung aktiviert werden.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Eine Arbeitskraft für die manuell Artikelneuzuordnung einrichten
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Lagerortverwaltung" > "Einrichtung" > "Arbeitskraft".
3. Klicken Sie auf "Bearbeiten".
4. Wählen Sie in der Liste Arbeitskraft 24 aus.
5. Erweitern Sie den Abschnitt Arbeit.
6. Wählen Sie "Ja" im Feld "Manuelle Artikelneuzuordnung zulassen" aus.

