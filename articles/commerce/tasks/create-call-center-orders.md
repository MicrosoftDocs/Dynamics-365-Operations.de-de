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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964844"
---
# <a name="create-call-center-orders"></a> Callcenteraufträge erstellen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für den Auftragssachbearbeiter vorgesehen. Voraussetzungen: Die Benutzer, welche das Verfahren ausführen, sind als Callcenterbenutzer eingerichtet, und der halbjährliche Fabrikam-Katalog wird mit mindestens einem Quellcode veröffentlicht.

1. Navigieren Sie zu **Einzelhandel und Handel \> Kunden \> Kundendienst**.
2. Geben Sie im Feld **SearchText** die Suchkriterien ein, um den Debitor zu suchen.
    * Für diese Beispielsprozedur geben Sie Karen ein und wählen **TAB**.  
3. Wählen Sie Suchen aus.
    * Da nur ein Debitor namens Karen in den Demodaten vorhanden ist, wird das Ergebnis automatisch ausgewählt.  
4. **Neuen Auftrag** auswählen.
5. Erweitern oder reduzieren Sie den Kopfbereich **Auftrag**.
6. Wählen Sie den Quelltyp für den Katalog aus.
    * Wenn keine aktiven Quellcodes vorliegen, können Sie diesen Schritt überspringen.  
7. Wählen Sie **Position hinzufügen** aus.
8. Geben Sie im Feld **Artikelnummer** den Artikelsuchbegriff ein.
    * Für diese Beispielprozedur geben Sie eine Artikelnummer 8111 ein und drücken Sie die Registerkarte. Durch diese Aktion wird das Artikelsuchfenster angezeigt.  
9. Wählen Sie das Produkt aus, das zum Auftrag hinzugefügt wird.
10. Geben Sie die Verkaufsmenge ein.
11. Wählen Sie **Erstellen** aus.
12. Wählen Sie **Abschließen**, um die Debitorenzahlung aufzuzeichnen.
13. Wählen Sie **Hinzufügen** aus.
    * Der Hinzufügen-Llink  ist die Registerkarte Zahlungen. Erweitern Sie die Registerkarte wenn sie verringert ist.  
14. Wählen Sie die Zahlungsmethode aus.
    * Für diese Prozedur wählen Sie die Bargeldzahlungsmethode aus.  
15. Schließen Sie die Seite.
16. Geben Sie den Betrag ein.
    * Für diese Prozedur geben Sie einen Betrag gleich dem Auftragssaldo ein, der in der Auftrags-Übersichtsseite auf der linken Seite des Betrag-Felds angezeigt werden kann. Dies Aktion ermöglicht Ihnen, den Auftrag als vollständig bezahlt abzuschließen.  
17. Wählen Sie **OK**.
18. Wählen Sie **Senden**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Transaktions-E-Mails nach Lieferart anpassen](../customize-email-delivery-mode.md)

[Lieferart in POS ändern](../pos-change-delivery-mode.md)

