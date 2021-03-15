---
title: Buchungen an Intrastat übertragen
description: Diese Prozedur zeigt Ihnen Schritt für Schritt, wie Sie Intrastat-Parameter einrichten und Transaktionen nach Intrastat übertragen.
author: Anasyash
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c9a5037f9e5381c61b72947d85bf07d571fe094d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982096"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Buchungen an Intrastat übertragen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen Schritt für Schritt, wie Sie Intrastat-Parameter einrichten und Transaktionen nach Intrastat übertragen. Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.


## <a name="create-new-and-update-existing-commodity-code"></a>Erstellen Sie einen neuen und aktualisieren Sie einen vorhandenen Warencode
1. Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Einstellungen > Kategorien und Attribute > Kategoriehierarchien**.
2. Suchen Sie in der Liste den Datensatz **Intrastat-Warencodes**, oder wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Wählen Sie in der Struktur einen Datensatz aus. Wählen Sie beispielsweise **Intrastat\Lautsprecher** aus.  
5. Klicken Sie auf **Bearbeiten**.
6. Erweitern Sie das Inforegister **Außenhandel**.
7. Geben Sie im Feld **Besondere Maßeinheit** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie beispielsweise **Stck.** aus.  
8. Wählen Sie **Ja** im Feld **Gewicht nicht anwendbar** aus.
9. Wählen Sie in der Struktur **Intrastat** aus.
10. Klicken Sie auf **Neuer Kategorieknoten**.
11. Geben Sie im Feld **Name** den Namen der Ware ein. Geben Sie beispielsweise **Andere Ware** ein.  
12. Geben Sie im Feld **Code** den Warencode ein. Geben Sie beispielsweise **995 00 00** ein.  
13. Geben Sie im Feld "Anzeigename" einen Wert ein. Geben Sie beispielsweise **Sonstige** ein.  
14. Klicken Sie auf **Speichern**.
15. Schließen Sie die Seite.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Weisen Sie Warencode zur Produkthierarchie und zum freigegebenen Produkt zu
1. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise nach dem Feld **Name** mit dem Wert **Vertrieb**.
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
3. Erweitern Sie **einen Kategorieknoten** in der Struktur. Erweitern Sie beispielsweise **Vertriebshierarchie\Audiogeräte für Zuhause**.  
4. Wählen Sie in der Struktur **die Kategorie aus, die dem Warencode zugewiesen werden soll**. Wählen Sie beispielsweise **Vertriebshierarchie\Audiogeräte für Zuhause\Lautsprecher** aus.  
5. Erweitern Sie das Inforegister **Warencodes**.
6. Klicken Sie auf **Hinzufügen**.
7. Wählen Sie im Feld **Hierarchie auswählen** die Option **Intrastat** aus.
8. Suchen Sie in der Liste den Warencode, und wählen Sie ihn aus. Wählen Sie beispielsweise **920 20 34 Lautsprecher** aus.  
9. Klicken Sie auf den Nach-rechts-Pfeil, um den Code auszuwählen.
10. Klicken Sie auf **OK**.
11. Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
12. Wählen Sie in der Liste das freigegebene Produkt aus, das Sie dem Warencode zuweisen. Wählen Sie beispielsweise **D0001** aus.  
13. Klicken Sie auf **Bearbeiten**.
14. Erweitern Sie das Inforegister **Außenhandel**.
15. Geben Sie im Feld **Ware** den Warencode ein. Wählen Sie beispielsweise den Wert **920 20 34 Lautsprecher** aus.    
16. Geben Sie im Feld **Prozentsatz für Belastungen** eine Zahl ein. Geben Sie beispielsweise **3** ein.  
17. Geben Sie im Feld **Land/Region** ein Ursprungsland oder eine Ursprungsregion ein oder wählen Sie diese(s) aus. Wählen Sie z. B. **AUT** aus.  
18. Erweitern Sie das Inforegister **Bestand verwalten**.
19. Geben Sie im Feld **Nettogewicht** ein Gewicht in kg ein. Geben Sie beispielsweise **2,5** ein.  
20. Klicken Sie auf **Speichern**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Richten Sie Intrastat-Transaktionscodes und Außenhandelsparameter ein
1. Wechseln Sie im Navigationsbereich zu **Module > Steuer > Einstellungen > Außenhandel > Art des Geschäftes**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Art des Geschäftes** einen Wert ein. Geben Sie beispielsweise **21** für den Transaktionscode ein, der als Rückgabe verwendet wird.  
4. Geben Sie im Feld **Name** den Namen des Transaktionscodes ein. Geben Sie beispielsweise **Rückgabe** ein.  
5. Wählen Sie im Feld **Statistikbetrag** eine Option aus. Wählen Sie beispielsweise **Leer** aus, was angibt, dass der statistische Wert, der für Transaktionen mit dem Transaktionscode **21** gemeldet werden soll, immer null ist.  
6. Wechseln Sie im Navigationsbereich zu **Module > Steuer > Einstellungen > Außenhandel > Außenhandelsparameter**.
7. Geben Sie im Feld **Art des Geschäftes** einen Wert ein, oder wählen Sie ihn aus. Wählen Sie z. B. **11** aus.  
8. Geben Sie im Feld **Gutschrift** einen Wert ein, oder wählen Sie einen Wert aus. Dieser Wert identifiziert zudem die physische Rückgabe. Die Gutschrift für die physische Rückgabe wird in die Intrastat-Erfassung mit entgegengesetzter Richtung übertragen. Beispielsweise wird die Rückgabe des Zugangs als Versand übertragen.   Andernfalls wird die Gutschrift als eine Korrektur betrachtet und wird mit der gleichen Richtung und entgegengesetztem Vorzeichen übertragen. Beispielsweise wird die Korrektur des Wareneingangs als Wareneingang mit negativem Betrag übertragen, und die aktive Markierung wird auf **Korrektur** festgelegt.  
9. Erweitern Sie das Inforegister **Übertragen**.
10. Wählen Sie **Ja** im Feld **Artikel mit Warencode** aus. Wählen Sie diese Option aus, um nur die Transaktionen mit einem zugewiesenen Warencode zu übertragen. Transaktionen ohne Warencode werden nicht an Intrastat übertragen.  
11. Wählen Sie im Feld **Umbuchen, wenn folgendes Kriterium erfüllt wird** eine Option aus. Wählen Sie beispielsweise **Einer der markierten** aus.  
12. Erweitern Sie den Abschnitt **Warencodehierarchie**.
13. Klicken Sie auf die Schaltfläche **Länder-/Regionseigenschaften**.
14. Klicken Sie auf **Neu**.
15. Wählen Sie im Feld **Land/Region** einen Wert aus, oder geben Sie einen Wert ein. Wählen Sie beispielsweise den Wert **FRA** aus.  
16. Geben Sie in das Feld **Intrastat-Code** den ISO-Code für das Land ein.  Geben Sie beispielsweise **FR** ein.  
17. Wählen Sie im Feld **Länder-/Regionsart** die Option **EU** aus.
18. Klicken Sie auf die Registerkarte "Nummernkreis".

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Richten Sie "Lieferarten" sowie Regeln zum Einschließen von Belastungen in Intrastat ein
1. Wechseln Sie im Navigationsbereich zu **Module > Vertrieb und Marketing > Einstellungen > Verteilung > Lieferarten**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie beispielsweise **20 Luft** aus.  
3. Erweitern Sie das Inforegister **Außenhandel**.
4. Klicken Sie auf **Bearbeiten**.
5. Geben Sie im Feld **Transport** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie z. B. **02** aus.  
6. Wechseln Sie im Navigationsbereich zu **Module > Debitorenkonten > Belastungen einrichten > Belastungscode**.
7. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld „Belastungscode“ mit dem Wert **Fracht**.
8. Erweitern Sie das Inforegister **Außenhandel**.
9. Klicken Sie auf **Bearbeiten**.
10. Wählen Sie **Ja** im Feld **Intrastat-Rechnungswert** aus. Der Betrag wird in das Feld **Rechnungszuschläge** übertragen und mit dem Betrag zusammengefasst, der im Feld „Rechnungsbetrag“ übertragen wird. Wählen Sie **Ja** im Feld **Intrastat-Statistikwert** aus, wenn der Betrag der Änderungen in das Feld **Statistikbelastungen** übertragen werden und mit **Statistikbetrag** zusammengefasst werden muss.  

## <a name="sell-products-for-eu-customers"></a>Verkaufen Sie Produkte für EU-Debitoren
1. Wechseln Sie im Navigationsbereich zu **Module > Debitoren > Aufträge > Alle Aufträge**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Feld **Debitorenkonto** einen EU-Debitor aus. Wählen Sie beispielsweise **DE-012 Litware Einzelhandel** aus.  
4. Erweitern Sie das Inforegister **Lieferung**.
5. Geben Sie im Feld **Lieferart** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie beispielsweise **20 Luft** aus.  
6. Klicken Sie auf **OK**.
7. Wählen Sie die erste Zeile von Auftragspositionen aus.
8. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie z. B. **D001** aus.  
9. Erweitern Sie das Inforegister **Positionsdetails**.
10. Klicken Sie auf die Registerkarte **Außenhandel**. Der Transport wird automatisch aus der ausgewählten Lieferart ausgefüllt.  
11. Geben Sie im Feld **Hafen** einen Wert ein, oder wählen Sie einen Wert aus.
12. Klicken Sie auf **Finanzdaten**. Gemäß den Einstellungen wird dieser Betrag in den **Intrastat-Rechnungswert** einbezogen.  
13. Klicken Sie auf **Belastungen verwalten**.
14. Geben Sie im Feld **Belastungscode** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie z. B. **FRACHT** aus.  
15. Aktivieren Sie das Kontrollkästchen **Beibehalten**.
16. Geben Sie im Feld **Wert der Belastungen** eine Zahl ein. Geben Sie beispielsweise **10** ein.  
17. Klicken Sie auf **Speichern**.
18. Schließen Sie die Seite.
19. Klicken Sie im Aktivitätsbereich auf **Rechnung**.
20. Klicken Sie auf **Rechnung**.
21. Erweitern Sie den Abschnitt **Parameter**.
22. Wählen Sie im Feld **Menge** die Option **Alle** aus.
23. Erweitern Sie das Inforegister **Einstellungen**.
24. Geben Sie im Feld **Rechnungsdatum** ein Datum ein. Geben Sie beispielsweise **31.01.2015** ein.  
25. Klicken Sie auf **OK**.
26. Klicken Sie auf **OK**.
27. Schließen Sie die Seite.
28. Klicken Sie auf **Neu**.
29. Wählen Sie im Feld **Debitorenkonto** einen EU-Debitor aus. Wählen Sie beispielsweise **DE-013 Trey-Großhandel** aus.
30. Klicken Sie auf **OK**.
31. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie z. B. **D0001** aus.  
32. Klicken Sie auf **Speichern**.
33. Klicken Sie auf **Rechnung**.
34. Geben Sie im Feld **Rechnungsdatum** ein Datum ein. Geben Sie beispielsweise das Datum **31.01.2015** ein.  
35. Klicken Sie auf **OK**.
36. Klicken Sie auf **OK**.

## <a name="transfer-transactions-to-the-intrastat"></a>Buchungen an Intrastat übertragen
1. Wechseln Sie im Navigationsbereich zu **Module > Steuer > Meldungen > Außenhandel > Intrastat**.
2. Klicken Sie auf **Übertragen**.
3. Wählen Sie **Ja** im Feld **Debitorenrechnung** aus.
4. Klicken Sie auf **Filter**.
5. Markieren Sie in der Liste die Zeile mit **Datum**.
6. Geben Sie im Feld **Kriterien** einen Wert ein. Geben Sie beispielsweise den Filter für die Periode "Januar 2015" ein (der genaue Wert hängt von Ihrem Datumsformat ab): 01.01.2015..31.01.2015  
7. Klicken Sie auf **OK**.
8. Klicken Sie auf **OK**.
9. Suchen Sie in der Liste den übertragenen Datensatz, und wählen Sie ihn aus.
10. Klicken Sie auf die Registerkarte **Allgemein**.
    
Überprüfen Sie die übertragenen Daten, einschließlich Land/Region des Ziels/der Lieferung, Ursprungsland, Gewicht, Menge, die Menge in zusätzlichen Einheiten, die Ware, der Transaktionscode, die Rechnungsbeträge und die statistischen Beträge. Sie können die Daten im Bedarfsfall ändern.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]