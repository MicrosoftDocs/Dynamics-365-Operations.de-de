---
title: Bestellungen erstellen
description: Dieser Artikel beschreibt den Prozess und die Optionen bei der manuellen Erstellung einer Bestellung.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: fbf5337ac41ceae6e911c056db5226c8ed1cefb0
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017

---

# <a name="create-purchase-orders"></a>Bestellungen erstellen

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Dieser Artikel beschreibt den Prozess und die Optionen bei der manuellen Erstellung einer Bestellung.

Beim Erstellen einer Bestellung (Purchase Order, PO) werden im Bestellkopf allgemeine Informationen über die gesamte Bestellung angegeben. Dann fügen Sie eine oder mehrere Bestellpositionen hinzu. Dieser Artikel beschreibt die hierzu häufig genutzt Optionen.  

Sie können auch POs erstellen, indem Sie Zeilen aus einem anderen Bestelldokument oder einem Auftragsdokument kopieren. In diesem Fall können Sie das Vorzeigen für den Bestand so umkehren, wie Sie das Vorzeichen auf einer Rechnung für eine Gutschrift umkehren.  

Obwohl POs manuell erstellen werden können, werden sie in der Regel von anderen Prozessen generiert. Aufträge können automatisch auf Basis andere Dokumente (z. B. Anforderungen) erstellt werden. Alternativ können sie als Teil des Produktprogrammplanungsprozesses durch geplante PO erstellt werden. Wenn von Rahmenbestellungen verwenden, können nach PO die **Freigabeauftrag** Aktivität erstellt werden. Es gibt außerdem erweiterte Methoden zum automatischen Erstellen einer Bestellung. Beispielsweise können Aufträge erstellt werden, wenn Sie die Direktlieferung oder Intercompany-Auftragsketten nutzen.

## <a name="creating-a-purchase-order-header"></a>Erstellen eines Bestellkopfs
Beim Erstellen einer neuen Bestellung wird ein Dialogfeld angezeigt, in dem Sie die häufigste Informationen für den Bestellkopf eingeben können. Beim Klicken auf **OK** um das Dialogfeld zu schließen, wird der Auftrag erstellt. Anschließend können Sie weitere Informationen in der Kopfzeile festlegen.  

Das erste Detail, das Sie bei der Erstellung einer Bestellung berücksichtigen müssen, ist der Typ des Auftrags. Der Typ **Bestellung** wird am häufigsten verwendet. Wenn ein Ausgleichsrechnung erforderlich ist, Sie können jedoch den Typ **Zurückgegebener Auftrag** nutzen.  

Sie müssen den Lieferanten im Feld **Kreditorenkonto** angeben. Für dieses Feld können Sie das Konto oder der Name des Kreditors suchen. Wenn ein Kreditor von mehreren Standorten aus liefert, jedoch nur einzelnes Rechnungskonto verwendet, können Sie dieses Rechnungskonto im Feld **Rechnungskonto** auswählen und es dann mit anderen Kreditorenkonten nutzen. Wenn Sie eine Bestellung für Produkte erstellen, die nicht wiederholt bestellt werden, können Sie die **Einmal-Lieferant**-Option nutzen. Diese Option erstellt automatisch ein neues Kreditorenkonto das als Einmalkonto markiert wird. So wird eine spätere Bereinigung für Einmalkonten im **Kreditorenkonten**-Modul unterstützt. Wenn Sie ein Kreditorenkonto auswählen, erben viele Felder im PO-Kopf Standardwerte aus den Informationen, die dem Kreditorenkonto zugeordnet sind. Beispielsweise werden der Standard-Lieferort und das Lager aus den Kreditorinformationen kopiert. Allerdings können Sie diese Standardwerte überschreiben, soll die Bestellung für einen anderen Standort vorgesehen sein.  

Wenn der Lieferant eine Referenznummer für den Auftrag angegeben hat, können diese Informationen im Feld **Kreditorenreferenz** erfasst werden. für zurückgegebene Aufträge müssen Sie einen Wert im Feld **RMA** angeben, um auf die Autorisierung des Lieferanten für die Verarbeitung der Rückgabe zu verweisen.  

Wenn ein Kaufvertrag mit dem Auftrag verknüpft ist, müssen Sie diese Informationen im Feld **Rahmenbestellung** angeben.  

Der PO-Header enthält auch Informationen zu Kosten, die für den gesamten Auftrag und nicht für einzelne Positionen gelten. Kosten können automatisch hinzugefügt werden, wenn automatische Zuschläge für den Kreditor oder Kreditorengruppe eingerichtet wurden. Sie können außerdem manuell Zuschläge im Auftragskopf hinzufügen, indem Sie auf **Zuschläge verwalten** im Aktivitätsbereich klicken.

## <a name="adding-purchase-order-lines"></a>Hinzufügen von Bestellpositionen
POs können für phyische Produkte oder Dienstleistungen gelten. Eine Einstellung für die Lagersteuerungsgruppe bestimmt, ob eine bestimmte Artikelnummer für ein Produkt oder eine Dienstleistung gilt. Gekauften Artikels wird in der Regel durch eine Artikelnummer angegeben. Wenn die Bestellung jedoch für direkt konsumierte Produkte oder Dienstleistungen gilt, können Sie auch mithilfe einer Beschaffungskategorie den Artikel angeben.  

Bestellzeilen enthalten viele Felder. Viele dieser Felder haben einen Standardwert oder einen Wert, der aus dem Auftragskopf übernommen wird. Zusätzliche Felder werden festgelegt, wenn Sie ein Produkt oder eine Dienstleistung auswählen. Die am häufigsten manuell festgelegten Felder sind die für Artikelnummern, die Menge und das gewünschte Lieferdatum. Informationen zum Verkaufspreis und zu Rabatten ist ebenfalls sehr wichtig. Die Werte dieser Felder hängen jedoch häufig von Handelsvereinbarung oder Rahmenverträgen ab.  

Wenn Sie ein Produkt auswählen, können Sie nach dem gesamten Produktnamen oder nach Teilen des Produktnamen statt nach der Artikelnummer suchen. Wenn das Produkt verschiedene Varianten, wie z. B. Größen hat, finden Sie eine Übersicht der verfügbaren Varianten über die Funktion **Positionen hinzufügen** oder über die Suche im Feld **Variantennummer**.  

Häufig müssen Sie mehrere Dimensionen für den ausgewählten Artikel für eine Bestellposition angeben. Die anzugebenden Dimensionen hängen von den Dimensionsgruppen ab, die in der Produktmasterdefinition zugewiesen wurden. Beispielsweise müssen häufig Sie einen Standort und Lagerort angeben, um den Lagerplatz anzugeben, an den das Produkt geliefert werden soll. Produktvarianten legen Sie fest, indem Sie die Variantennummer angeben oder indem Sie Werte für eine oder mehrere Produktdimensionen wie Farbe, Größe, Konfiguration oder Stil eingeben. Mit Rückverfolgungsangaben, wie Chargen- oder Seriennummern, können Sie einen Lagerartikel eindeutig identifizieren. Nach der Erstellung eines Auftrags erfassen Sie mit der Aktion **Registrierung** Dimensionswerte zum Auftrag. Sie bestellen beispielsweise fünf Stück eines Artikels. Später registrieren Sie, das drei Artikel schwarz und zwei blau sein sollen. Dieser Ansatz ist eine Alternative zum Erfassen von Dimensionsinformationen während der Wareneingangsregistrierung.  

Sie können die Details des Lagerbuchungsstatus für gelagerte Produkte überprüfen. Sie möchten z. B. den Lagerbestand prüfen, um die Bestellmenge festzulegen. Alternativ können Sie den Lagerstatus einer bestellten Menge prüfen, um zu sehen, ob die Wareneingangsregistrierung stattgefunden hat.  

Eine Bestellposition für eine Rückgabe an den Kreditor hat eine negative Menge. Sie können über die Aktion **Reservierung** eine bestimmte Charge für die Rückgabe auswählen.  

Manchmal möchten Sie die bestellte Menge teilen, so dass verschiedene Teile des an unterschiedlichen Tagen geliefert werden. Diese Lieferungen können Sie über die Aktion **Lieferzeitplan** einrichten. Sie finden sie im Menü **Bestellposition** in der Ansicht **Positionen**.  

Kosten können automatisch zu PO-Positionen hinzugefügt werden wenn automatische Zuschläge für den Kreditor oder Kreditorenzuschlagsgruppe und für den Artikel oder die Artikelzuschlagsgruppe eingerichtet wurden. Normalerweise werden Zuschläge jedoch manuell zum jeweiligen Auftrag hinzugefügt. Um eine Belastung hinzuzufügen, öffnen die Seite **Belastungen verwalten**, indem Sie die Aktion **Belastungen verwalten** im Menü **Finanzdaten** in der Ansicht **Positionen** nutzen. Der Vorteil beim Hinzufügen von Belastungen auf Bestellebene ist, dass die Belastung als Lagerkosten zugeordnet werden kann. Um Belastungscodes für Produktkosten einzurichten, verwenden Sie die Belastungsoption **Artikel**. Derartige Belastungstypen müssen vor der Genehmigung der Bestellung aus dem Bestellungskopf zugeordnet werden. Sie möchten z. B. Belastungen basierend auf der Menge in jeder Position zuweisen. Die Belastungskategorie wirkt sich auch darauf aus, wie die Belastungen berücksichtigt werden. Feste Belastungen legen beispielsweise einen festen Betrag fest. Prozentuale Belastungen werden als Prozentsatz des Nettobetrags für die Auftragsposition berechnet. POs können einer Auslastung zugewiesen werden. Die Auslastung kann eine Schätzung der erwarteten Ausgaben für die Transportkosten enthalten. Sie können diese Ausgabe von der Auslastung zurück zu den Bestellungspotionen zuweisen.

## <a name="purchase-order-actions"></a>Bestellungsaktionen
Nachdem Sie den Kopf und die Positionen zur Bestellung hinzugefügt haben, müssen Sie oft zusätzliche Schritte ausführen, bevor die Bestellung bestätigt werden kann. Da so viele Optionen verfügbar sind, ist es unter Umständen hilfreich, die entsprechende Menüelement über [Aktion suchen](/dynamics365/unified-operations/fin-and-ops/get-started/action-search) zu suchen.  

Sie können Produkte in der Bestellung so konfigurieren, dass sie zusätzliche Artikel haben. Zusätzliche Artikel sind Produkte, die zusammen mit anderen Produkten erworben werden müssen oder erworben werden können. Zusätzliche Produkte können kostenlos als zugehörige Produkte hinzufügt werden. Möglicherweise können Sie entscheiden, ob sie dem Auftrag hinzufügen oder nicht hinzugefügt werden. Sie können die zusätzlichen Artikel nach jeder Auftragsposition die hinzugefügt wird überprüfen. Möglicherweise ist es jedoch einfacher, die zusätzlichen Artikel für alle Auftragspositionen über die Seite **Zusätzliche Artikel** zu überprüfen. Diese können sie über den Aktionsbereich öffnen.  

Rabatte werden normalerweise beim Erstellen von Positionen hinzugefügt. Allerdings gelten einige Rabatte für den gesamten Auftrag:

-   Die Aktion **Rechnungsrabatt:** berechnet einen Prozentsatz, der für die gesamte Bestellung gilt. Verwechseln Sie diesen Rabatt nicht mit dem Skonto-Rabattprozentsatz. Skonti werden angewendet, wenn die Rechnung bezahlt ist. Sie hängen vom Zahlungsausgleich nach einem bestimmten Datum ab.
-   Wenn ein Rabatt für mehrere Positionen gilt, müssen Sie die Aktion **Sammelrabatt** zum Berechnen und Zuordnen zur Bestellung nutzen. Sammelrabatte sind Rabatte, die angeboten werden können, wenn eine Kombination von Produkten in der Bestellung einen gemeinsamen Schwellenwert übersteigt. Nur wenige Unternehmen verwenden diese Art von Rabatt.

Belastungen, die einen Belastungscode haben, der den **Artikel**-Solltyp verwendet, müssen auf Positionsebene zugewiesen werden, bevor die Bestellung bestätigt werden kann. Es sinnvoll, diese Zuschläge auf der Auftragskopfebene zuzuweisen. So können Sie den Gesamtbetrag der Belastungen festlegen. Jedoch muss in diesem Fall die Belastung jeder Position zugeordnet werden, bevor die Bestellung bestätigt werden kann. Sie können die Aktion **Belastungen zuordnen** nutzen, um Beträge aus Belastungen zu Teilen, die auf Kopfebene den Auftragspositionen zugeordnet sind. Belastungen können nach dem Nettobetrag jeder Position, nach der bestellten Menge oder gleichmäßig unter allen Positionen geteilt werden. Nachdem Sie Belastungen zu Positionen zugewiesen haben, wird die Belastung aus dem Auftragskopf entfernt.  

POs können so konfiguriert werden, dass vor ihrer Verarbeitung Budgetmittel zur Bestellung zugewiesen werden müssen. In diesem Fall können Sie die Aktion **Budgetprüfung** zur Zuordnung des Budgets nutzen.  

Möglicherweise müssen Sie den Abschluss einer Bestellung verzögern. Beispielsweise benötigen Sie weitere Informationen über Produkte oder Dienstleistungen oder möglicherweise eine Autorisierung für die Ausgabe. Es gibt verschiedene Möglichkeiten, um eine Bestellung zurückzuhalten. Beispielsweise können Sie warten bis Sie den Auftrag bestätigen. Bei einem Change Management-Workflow kölnnen Sie die Bestellung alternativ nicht zur Genehmigung senden. Wenn Sie alle Bestellungen für einen bestimmten Kreditor blockieren müssen, können Sie auch den Kreditor in den Masterdaten als für die Verarbeitung **Gesperrt** markieren. Es gibt auch Umstände, die die Verarbeitung der Bestellung verhindern. Die Verarbeitung kann beispielsweise verhindert werden, wenn das Kreditlimit überschritten ist oder wenn erforderliche Budgetmittel nicht verfügbar sind.

<a name="see-also"></a>Siehe auch
--------

[Überblick über Bestellungen](purchase-order-overview.md)

[Genehmigen und Bestätigen von Bestellungen](purchase-order-approval-confirmation.md)

[Produkteingang für Bestellungen](product-receipt-against-purchase-orders.md)

[Überblick über Kreditorenrechnungen](/dynamics365/unified-operations/financials/accounts-payable/vendor-invoices-overview)




