---
title: Anschlussprogramme nutzen
description: Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58eca42634ad995f174350bc3a1996ddc4c449b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804088"
---
# <a name="using-continuity-program"></a>Anschlussprogramme nutzen

[!include [banner](../includes/banner.md)]

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
15. Navigieren Sie zu Einzelhandel und Handel > Anschluss > Anschlusszahlungen verarbeiten.
16. Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
17. Klicken Sie auf "OK".
18. Navigieren Sie zu Einzelhandel und Handel > Anschluss > Untergeordnete Anschlussaufträge erstellen.
    * Dieser Prozess erstellt neue Aufträge auf Grundlage der Einstellungen der Kontinuitätsprogramme.  
19. Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.
    * Artikel '88000' ist ein Anschlussartikel in den USRT-Demodaten.  
20. Geben Sie im Feld 'Auftrag' einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie die Auftragsnummer ein, die Sie weiter oben in der Prozedur notiert haben. So bleibt die Verarbeitungszeit für dieses Verfahren minimal. Das Auftragsfeld ist optional. Sie können alle Aufträge für ein beliebiges Programm verarbeiten.  
21. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]