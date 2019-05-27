---
title: " Callcenteraufträge erstellen"
description: Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4867ad67dc570ab42420ba12fc7dc2da6b5ba503
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548254"
---
# <a name="create-call-center-orders"></a> Callcenteraufträge erstellen

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für den Auftragssachbearbeiter vorgesehen. Voraussetzungen: Die Benutzer, welche das Verfahren ausführen, sind als Callcenterbenutzer eingerichtet, und der halbjährliche Fabrikam-Katalog wird mit mindestens einem Quellcode veröffentlicht.

1. Navigieren Sie zu Einzelhandel und Handel > Kunden > Kundendienst.
2. Geben Sie im SearchText-Feld die Suchkriterien ein, um den Debitor zu suchen.
    * Für diese Beispielsprozedur geben Sie "karen" ein und drücken Sie die Taste.  
3. Klicken Sie auf "Suchen".
    * Da nur ein Debitor namens Karen in den Demodaten vorhanden ist, erfolgt die Auswahl automatisch.  
4. Klicken Sie auf "Neuer Auftrag".
5. Erweitern oder reduzieren Sie den Kopfbereich "Auftrag".
6. Wählen Sie den Quelltyp für den Katalog aus.
    * Wenn keine aktiven Quellcodes vorliegen, können Sie das Quellfeld schließen und diesen Schritt überspringen.  
7. Klicken Sie auf "Position hinzufügen".
8. Geben Sie im Feld "Artikelnummer" den Artikelsuchbegriff ein.
    * Für diese Beispielprozedur geben Sie eine Artikelnummer " 8111 "ein und drücken Sie die Registerkarte. Dadurch wird das Artikelsuchfenster angezeigt.  
9. Wählen Sie das Produkt aus, das zum Auftrag hinzugefügt werden soll.
10. Geben Sie die Verkaufsmenge ein.
11. Klicken Sie auf Erstellen.
12. Klicken Sie auf "Abschließen", um die Debitorenzahlung aufzuzeichnen.
13. Klicken Sie auf Hinzufügen.
    * Der Hinzufügen-Llink  ist die Registerkarte Zahlungen. Erweitern Sie die Registerkarte wenn sie verringert ist.  
14. Wählen Sie die Zahlungsmethode aus.
    * Für diese Prozedur wählen Sie die Bargeldzahlungsmethode aus.  
15. Schließen Sie die Seite.
16. Geben Sie den Betrag ein.
    * Für diese Prozedur geben Sie einen Betrag gleich dem Auftragssaldo ein, der in der Auftrags-Übersichtsseite auf der linken Seite des Betrag-Felds angezeigt wird. Dies ermöglicht Ihnen, den Auftrag als vollständig bezahlt abzuschließen.  
17. Klicken Sie auf "OK".
18. Klicken Sie auf Absenden.

