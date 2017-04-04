---
title: Rechnungsabgleich und Intercompany-Bestellungen
description: "Die einkaufende juristische Person, die in eine Buchung des Intercompany-Handels einbezogen ist, kann auch so eingerichtet werden, dass der Kreditorenrechnungsabgleich verwendet wird. In diesem Fall müssen sowohl die Buchungsanforderungen für den Intercompany-Handel und der Kreditorenrechnungsabgleich erfüllt sein, bevor Intercompany-Kreditorenrechnungen gebucht werden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 45d0b24ed0a79176803a6efefc216f7e30fec86c
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Rechnungsabgleich und Intercompany-Bestellungen

Die einkaufende juristische Person, die in eine Buchung des Intercompany-Handels einbezogen ist, kann auch so eingerichtet werden, dass der Kreditorenrechnungsabgleich verwendet wird. In diesem Fall müssen sowohl die Buchungsanforderungen für den Intercompany-Handel und der Kreditorenrechnungsabgleich erfüllt sein, bevor Intercompany-Kreditorenrechnungen gebucht werden können.

Die Beispiele in diesem Thema verwenden die folgenden Einstellungen für den Intercompany-Handel:
-   Fabrikam Purchase ist die einkaufende juristische Person.
-   Fabrikam Sales ist die verkaufende juristische Person.
-   In Fabrikam Verkauf ist der Debitor "4020" vorhanden.
-   In Fabrikam Einkauf ist der Kreditor "3024" vorhanden.
-   In "Fabrikam Einkauf werden Intercompany-Informationen für Kreditor" 3024 " angegeben. " Ist als das angegebene Kundenunternehmen erhaltene, Debitor und 4020 wird als das angegebene Debitorenkonto, das der Einkauf-juristischenPerson Fabrikam entspricht.
-   In werden Intercompany-Informationen für Debitor " 4020 angegeben. Fabrikam Einkauf " wird zum Kreditorenunternehmen angegeben, Kreditor und 3024 wird als das angegebene Kreditorenkonto, das der Fabrikam-Vertriebsjuristischen Person entspricht.

In den Beispielen werden für Fabrikam Purchase die folgenden Einstellungen für den Kreditorenrechnungsabgleich verwendet:
-   Auf der Seite Kreditorenparameter wird die Option zum Aktivieren der Rechnungsabgleichüberprüfung ausgewählt.
-   Auf der Seite Kreditorenparameter wird das Feld „Rechnung mit Abweichungen buchen“ auf „Genehmigung anfordern“ gesetzt.
-   Die Preistoleranzprozentsatz für die juristische Person liegt bei 2 %.

## <a name="example-price-matching-and-intercompany-trade"></a>Beispiel: Preisabgleich und Intercompany-Handel
Die Nettobeträge für die Intercompany-Kreditorenrechnung und die Intercompany-Debitorenrechnung müssen übereinstimmen. Durch diese Anforderung werden alle anderen Rechnungsabgleichsgenehmigungen oder Preistoleranzprozentwerte außer Kraft gesetzt. Sie führen beispielsweise die folgenden Schritte durch.
1.  In "Fabrikam Einkauf Auftrag erstellen SO888 für Debitor" 4020. Intercompany-Bestellung " ICBE222 wird automatisch für Kreditor "3024 "in" Fabrikam Einkauf und Auftrag "ICAU888" erstellt, wird automatisch in " erstellt.
2.  Registrieren Sie in Fabrikam Sales, dass die Artikel eingegangen sind, und buchen Sie einen Lieferschein. Der Status von "ICAU888" wechselt zu "Geliefert". Der Status von "ICBE222" wechselt zu "Eingegangen".
3.  In Fabrikam Sales nehmen Sie eine Rechnungsaktualisierung für ICSO888 vor. Der Einheitenpreis beträgt "0,45", und 100 Artikel werden aktualisiert.
4.  Sie erstellen in Fabrikam Purchase eine Rechnung für ICPO222. Der Nettopreis wird versehentlich von "45,00" zu "54,00" geändert. Ein Symbol zeigt an, dass der Preis über der zulässigen Preistoleranz von 2 Prozent liegt.
5.  Wählen Sie auf der Seite Rechnungsabgleichsdetails wählen Sie die Option aus, Buchung mit Abweichungen zu genehmigen. Klicken Sie auf der Seite Kreditorenrechnung auf OK. Wenn die Kreditorenrechnung keine Intercompany-Kreditorenrechnung war, würde die Buchung erfolgreich sein. Da Sie jedoch mit einer Intercompany-Kreditorenrechnung arbeiten, muss die Buchung fehlgeschlagen. Für den Intercompany-Handel müssen die Rechnungssummen im Intercompany-Auftrag den Rechnungssummen auf der entsprechenden Intercompany-Bestellung entsprechen. Um dieses Problem zu beheben, müssen Sie den Nettopreis auf der Rechnung korrigieren, indem Sie den Nettopreis wieder zum Standardbetrag 45,00 ändern.

## <a name="example-quantity-matching-with-intercompany-trade"></a>Beispiel: Mengenabgleich mit Intercompany-Handel
Die Mengen auf der Intercompany-Bestellung und auf dem Intercompany-Auftrag müssen übereinstimmen. Durch diese Anforderung werden alle anderen Rechnungsabgleichsgenehmigungen außer Kraft gesetzt. In diesem Beispiel werden für den Intercompany-Handel die folgenden zusätzlichen Einstellungen eingerichtet:
-   In Fabrikam Purchase wird die Bestellungsaktivitätsrichtlinie für Kreditor 3024 installiert, um die Debitorenrechnung und die Intercompany-Kreditorenrechnung automatisch zu buchen.

In diesem Beispiel werden für Fabrikam Einkauf die folgenden zusätzlichen Einstellungen für den Kreditorenrechnungsabgleich verwendet:
-   Auf der Artikelmodellgruppenseite für die Modellgruppe, die durch den Artikel B-R14 verwendet wird, wird die Option Empfangsanforderungen ausgewählt.
-   Der verfügbare Bestand des Artikels "B-R14" beträgt 0 (Null).

Sie führen beispielsweise die folgenden Schritte durch.
1.  In "Fabrikam Einkauf Auftrag erstellen SO999 für Debitor" 4020. Der Auftrag enthält einen Positionsartikel: 100 Batterien (Artikel "B-R14") zu einem Einheitenpreis von jeweils " 1,00 ". In Fabrikam Purchase wird für den Kreditor 3024 automatisch die Intercompany-Bestellung "ICPO333 erstellt, und in Fabrikam Sales wird der Auftrag ICSO999 erstellt.
2.  In Fabrikam Sales nehmen Sie eine Rechnungsaktualisierung für ICSO999 vor. Die Buchung schlägt fehl, da der Artikel nicht vorrätig ist und noch nicht eingegangen ist. Daher können die Finanzdaten nicht aktualisiert werden.
3.  Sie erfassen den Eingang des Artikels und buchen in Fabrikam Sales einen Lieferschein für ICSO999. Ein Produktzugang für ICPO333 wird automatisch in Fabrikam Purchase gebucht. Die eingegangene Menge des Artikels "B-R14" wird in Fabrikam Purchase zu "100" geändert.
4.  In Fabrikam Sales nehmen Sie eine Rechnungsaktualisierung für ICSO999 vor. Die Buchung ist in beiden juristischen Personen erfolgreich. Die erworbene Menge des Artikels "B-R14" wird in Fabrikam Purchase zu "100" geändert.




