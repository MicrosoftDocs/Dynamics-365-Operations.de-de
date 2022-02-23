---
title: Anschlussprogramme nutzen
description: Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412594"
---
# <a name="using-continuity-program"></a>Anschlussprogramme nutzen

[!include [banner](../includes/banner.md)]

Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge. Damit sie dieses Verfahren abschließen können, muss der Benutzer als Callcenterbenutzer eingerichtet werden. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Navigieren Sie zu Retail und Commerce > Kunden > Kundendienst.
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
15. Navigieren Sie zu Retail und Commerce > Anschluss > Anschlusszahlungen verarbeiten.
16. Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
17. Klicken Sie auf "OK".
18. Navigieren Sie zu Retail und Commerce > Anschluss > Untergeordnete Anschlussaufträge erstellen.
    * Dieser Prozess erstellt neue Aufträge auf Grundlage der Einstellungen der Kontinuitätsprogramme.  
19. Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
    * Artikel '88000' ist ein Anschlussartikel in den USRT-Demodaten.  
20. Geben Sie im Feld 'Auftrag' einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie die Auftragsnummer ein, die Sie weiter oben in der Prozedur notiert haben. So bleibt die Verarbeitungszeit für dieses Verfahren minimal. Das Auftragsfeld ist optional. Sie können alle Aufträge für ein beliebiges Programm verarbeiten.  
21. Klicken Sie auf "OK".

