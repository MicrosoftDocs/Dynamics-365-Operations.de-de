--- 
title: "Verkauf von Anschlussprogrammen und Verarbeitung zugehöriger Aufträge"
description: "Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 5fe1823c9b684bbc5ac5bd0871cc5c0a0e6ce678
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="selling-continuity-programs-and-processing-related-sales-orders"></a>Verkauf von Anschlussprogrammen und Verarbeitung zugehöriger Aufträge

[!include [task guide banner](../includes/task-guide-banner.md)]

Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge. Damit sie dieses Verfahren abschließen können, muss der Benutzer als Callcenterbenutzer eingerichtet werden. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Navigieren Sie zu Einzelhandel und Handel > Kunden > Kundendienst.
2. Geben Sie im Suchtext-Feld "Karin" ein, und drücken Sie dann die TAB-Taste.
    * Das Dialogfeld für die erweiterte Suche wird angezeigt. Wenn dies nicht der Fall ist, klicken Sie rechts neben diesem Feld auf Suchen.  
3. Markieren Sie in der Liste die ausgewählte Zeile.
    * Es darf nur eine Zeile mit "Karin Berg" geben. Wählen Sie die Zeile aus, indem Sie auf die auf Häkchenspalte am linken äußeren Rand des Formulars klicken.  
4. Klicken Sie auf Auswählen.
5. Klicken Sie auf "Neuer Auftrag".
    * Es empfiehlt sich, die Auftragsnummer zu notieren. Sie benötigen Sie sie später in diesem Verfahren.  
6. Geben Sie im Artikelnummer-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
    * Dies ist ein Anschlussartikel in den USRT-Demodaten.  
7. Klicken Sie auf "Abgeschlossen".
8. Geben Sie im Feld "Zahlungsmethode" "Visa" aus.
9. Klicken Sie auf "Kreditkarte hinzufügen".
    * Geben Sie die erforderlichen Kreditkarteninformationen auf dieser Seite ein.  
10. Klicken Sie auf "OK".
11. Erweitern Sie den Abschnitt "Zahlung".
    * Um einen Callcenterauftrag zu senden, müssen die Zahlungen für den Auftrag eingegeben werden.  
12. Klicken Sie auf "OK".
13. Klicken Sie auf Absenden.
    * Sie haben einen neuen Anschlussauftrag erstellt. Als nächstes führen Sie zwei Stapelverarbeitungsvorgänge aus, die verwendet werden, um die Kontinuitätsaufträge zu verarbeiten.  
14. Schließen Sie die Seite.
15. Navigieren Sie zu Einzelhandel und Handel > Anschluss > Anschlussprogramme verarbeiten.
16. Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
17. Klicken Sie auf "OK".
18. Navigieren Sie zu Einzelhandel und Handel > Anschluss > Untergeordnete Anschlussaufträge erstellen.
    * Dieser Prozess erstellt neue Aufträge auf Grundlage der Einstellungen der Kontinuitätsprogramme.  
19. Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
    * Artikel '88000' ist ein Anschlussartikel in den USRT-Demodaten.  
20. Geben Sie im Feld 'Auftrag' einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie die Auftragsnummer ein, die Sie weiter oben in der Prozedur notiert haben. So bleibt die Verarbeitungszeit für dieses Verfahren minimal. Das Auftragsfeld ist optional. Sie können alle Aufträge für ein beliebiges Programm verarbeiten.  
21. Klicken Sie auf "OK".


