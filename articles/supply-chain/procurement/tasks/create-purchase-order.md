---
title: Eine Bestellung erstellen
description: Dieses Thema zeigt Ihnen, wie Sie eine Bestellung manuell erstellen.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec91174f291bcfa7027a93ca344823561cc29e3f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429097"
---
# <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

[!include [banner](../../includes/banner.md)]

Dieses Thema zeigt Ihnen, wie Sie eine Bestellung manuell erstellen. Es ist aber typischer, dass Bestellungen automatisch als Ergebnis des Produktprogrammplans, der Direktlieferung und anderer Prozesse erstellt werden. Bestellungen werden normalerweise von einem Einkaufsvertreter erstellt. Das Beispiel, das hier angezeigt wird, kann im USMF-Demodatunternehmen verwendet werden. Dabei können die Werte verwendet werden, die in den Hinweisen für verschiedene Schritte vorgeschlagen werden.


## <a name="create-the-purchase-order-header"></a>Erstellen Sie den Bestellkopf
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Bestellungen > Alle Bestellungen**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie das Kreditorenkonto **US-101** aus. Wenn Sie einen Händler auswählen, werden Details aus einem Kreditorendatensatz wie Adresse, Rechnungskonto, Lieferbedingungen und Lieferart als Standardwerte in den Auftragskopf kopiert. Die können diese Werte jederzeit ändern.  
4. Erweitern Sie den Abschnitt **Allgemein**.

    - Das Feld **Standort** zusammen mit dem Feld **Lagerort** gibt an, wohin die beschafften Waren oder Dienstleistungen geliefert werden müssen. Die Standardlieferadresse ist der Standort. Beide Felder können mit Werten aufgefüllt werden, die für den ausgewählten Händler eingerichtet wurden, oder Sie können diese manuell angeben.  
    - Das Feld **Lieferdatum** wird verwendet, um anzugeben, wann beschaffte Waren und Dienstleistungen geliefert werden müssen. Sie können ein einzelnes Lieferdatum für den Auftrag angeben, oder für die einzelnen Auftragspositionen können eindeutige Lieferdaten angegeben werden. Kann das Lieferdatum, das hier angegeben ist, nicht für bestimmte Produkte oder Dienstleistungen erfüllt werden, da sie längere Durchlaufzeiten haben, dann werden diese Positionen mit einem späteren Lieferdatum erstellt, um dies zu berücksichtigen.  

5. Erweitern Sie den Abschnitt **Verwaltung**. Das Feld **Auftraggeber** kann verwendet werden, um anzugeben, wer den Auftrag erteilt. Es kann möglicherweise vorteilhaft sein, dies dem Händler freizugeben, falls jener mit dieser Person Rücksprache halten muss. Dem Feld kann automatisch ein Wert zugewiesen werden, wenn das aktuelle Benutzerkonto einem Namen auf der Seite **Benutzer** zugeordnet ist.  
6. Wählen Sie **OK**. Der Auftragskopf ist jetzt erstellt worden. Wenn Sie mit Bestellpositionen arbeiten, wird nur eine Zusammenfassung der Kopfinformationen angezeigt. Wenn Sie die restlichen Informationen anzeigen möchten, wählen Sie **Kopf** aus.  

## <a name="add-a-purchase-order-line"></a>Fügen Sie eine Bestellposition hinzu
1. Wählen Sie **Bestellposition**.
2. Wählen Sie **Dimensionen** aus. Produkte können in Varianten sein, die in Dimensionen wie Farbe, Größe oder Stil unterschieden werden. Produkte können auch so eingerichtet werden, dass Lagerdimensionen, wie Standort und Lagerort zu verwenden sind. Es gibt auch optionale Rückverfolgungsangaben, wie Chargen- und Seriennummern. Um die Effizienz der Auftragserfassung zu verbessern, können Sie die Dimensionsfelder, die Sie im Allgemeinen verwenden, direkt zum Auftragsraster hinzufügen.  
3. Aktivieren Sie das Kontrollkästchen **Farbe**. Optional: Wenn Sie das Feld **Einstellungen speichern** auswählen, werden die Dimensionen, die Sie ausgewählt haben, beim nächsten Mal, wenn Sie die Bestellungsseite öffnen, auch im Auftragspositionsraster angezeigt.  
4. Wählen Sie **OK**.
5. Wählen Sie im Feld **Artikelnummer** die Option **T0004** aus.

    - Auftragspositionen werden für Produkte und Dienstleistungen erstellt, indem eine Artikelnummer angegeben wird, oder als Ausgaben, indem eine Beschaffungskategorie angegeben wird. 
    - Das Kategoriefeld **Beschaffung** wird für das Hinzufügen von Positionen verwendet, bei denen der beschaffte Artikel direkt ausgegeben werden, anstatt in den Bestand zu gelangen. Das bedeutet, dass wenn Sie einen Einkauf tätigen müssen, Sie diesen Schritt ausführen können, indem Sie eine Bestellposition erstellen, die eine Beschaffungskategorie angibt, anstatt eine Position mit einer Artikelnummer zu erstellen. Artikel können auch einer Beschaffungskategorie zugeordnet werden und in diesem Fall wird die Beschaffungskategorie nur zu Informationszwecken angezeigt.  

6. Geben Sie im Feld **Farbe** einen Wert ein oder wählen Sie einen Wert aus. Die Felder **Standort** und **Lagerort** werden in der Regel mit Werten aus dem Auftragskopf aufgefüllt, es ist jedoch möglich, die Felder zu überschreiben, wenn manche Positionen an verschiedene Orte geliefert werden müssen.  
7. Geben Sie im Feld **Menge** eine Zahl ein.

    - Wählen Sie die Menge aus, die Sie einkaufen möchten. Das Feld **Menge** wird automatisch mit der minimalen Auftragsmenge für das Produkt aufgefüllt, wenn dies eingerichtet ist, oder mit dem Wert von 1.  
    - Das Feld **Einheit** gibt die Maßeinheit für die bestellte Menge an. Normalerweise wird die Einheit automatisch aus der Bestelleinheit auf den Produktmasterdaten bereitgestellt, Sie können dies jedoch ändern.  
    - Das Feld **Preis je Einheit** enthält üblicherweise einen Wert entweder aus einem Kaufvertrag oder aus einer Handelsvereinbarung. Es ist möglich, den Preis je Einheit für einzelne Auftragspositionen zu ändern, beispielsweise dann, wenn ein eindeutiger Preis mit dem Händler ausgehandelt wird.  
    - Das Feld **Rabatt** stellt einen Rabattbetrag pro Einheit dar. Dieser Rabatt verringert daher den Preis je Einheit um den Rabatt. Dieser Rabatt wird im Allgemeinen automatisch in Kaufverträgen oder Handelsvereinbarungen angegeben, kann jedoch bei einzelnen Positionen überschrieben werden, wenn eindeutige Rabatte mit dem Händler ausgehandelt wurden.  
    - Ein Rabattprozentsatz kann eingegeben werden, der den Nettobetrag für die Position entsprechend reduziert. Der Rabattprozentsatz wird oft automatisch in Kaufverträgen oder Handelsvereinbarungen angegeben, kann jedoch bei einzelnen Positionen überschrieben werden, wenn ein eindeutiger Rabattprozentsatz mit dem Händler ausgehandelt wurde.  
    - Der Wert im Feld **Nettobetrag** wird aus anderen Feldern zur Position einschließlich Menge, Preis je Einheit, Rabatt und Rabattprozentsatz berechnet. Es ist möglich, den Nettobetrag zu ändern, dann sind jedoch die Felder **Preis je Einheit**, **Rabatt** und **Rabatt in Prozent** leer. Wenn Sie auf die Position buchen, wird der gebuchte Betrag proportional zum Nettobetrag sein. Normalerweise wird das Feld **Nettobetrag** nur für die Anzeige des Nettobetrags der Position verwendet.  

8. Erweitern Sie den Abschnitt **Positionsdetails**.
9. Wählen Sie die Registerkarte **Lieferung** aus. Ein eindeutiges Lieferdatum kann jeder Auftragsposition zugewiesen werden. Das Datum wird aus dem Feld im Bestellkopf übernommen, Sie können dies jedoch ändern.  

## <a name="review-order-totals"></a>Prüfen Sie Auftragssummen
1. Wählen Sie **Summen** aus.

    - Wenn Sie die Aktivität **Summen** nicht sehen, wählen Sie die Registerkarte **Bestellung** im Aktivitätsbereich aus.  
    - Dieses Dialogfeld zeigt die Summen für den gesamten Auftrag an.  
    - Das Feld **Auswahl** ermöglicht es Ihnen, die Grundlage zu ändern, auf der Summen berechnet werden. So können Sie beispielsweise auswählen, dass die **Menge im Produktzugang** Summen anzeigt, die dem Betrag des Produkts/der Produkte zugeordnet ist/sind, die eingegangen sind, oder Sie können auswählen, dass **Bestellte Menge** die Menge der Produkte anzeigt, die bestellt wurden.  

2. Wählen Sie **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]