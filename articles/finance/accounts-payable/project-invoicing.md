---
title: Projektrechnungsstellung
description: Dieses Thema enthält einen Überblick über die Projektrechnungsstellung für Zeit- und Materialprojekte und Festpreisprojekte. Er umfasst Informationen zu Rechnungsvorschlägen (vorläufige Rechnungen), Rechnungskontrolle, Akonto-Rechnungsstellung, Kreditorenrechnungsstellung und Gutschriften.
author: TaylorVH
manager: AnnBe
ms.date: 07/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5a6a29b180564dc4e4dd768b9e4b97c8877ce00c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979586"
---
# <a name="project-invoicing"></a>Projektrechnungsstellung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält einen Überblick über die Projektrechnungsstellung für Zeit- und Materialprojekte und Festpreisprojekte. Er umfasst Informationen zu Rechnungsvorschlägen (vorläufige Rechnungen), Rechnungskontrolle, Akonto-Rechnungsstellung, Kreditorenrechnungsstellung und Gutschriften.

Das zu verwendende Fakturierungsverfahren wird durch den Projekttyp bestimmt. Eine Fakturierung kann ausschließlich für die beiden externen Projekttypen Aufwand und Festpreis erfolgen. Aufwands- und Festpreisprojekte sind immer einem Projektvertrag zugeordnet.

-   **Festpreisprojekte** – Der Debitorenrechnungsbetrag basiert auf Rechnungsfakturierungsplänen. Die Fakturierung erfolgt anhand von Akontoeinstellungen, die auch als Fakturierungsplan bezeichnet werden. Festpreisprojekte können pro Projekt oder pro Projektvertrag fakturiert werden.
-   **Aufwandsprojekte** – Der Debitorenrechnungsbetrag basiert auf Buchungspositionen, die für Projekte eingegeben werden. Buchungen für Aufwandsprojekte können pro Projekt oder pro Projektauftrag fakturiert werden.

Aufwands- und Festpreisprojekte können den Rechnungsprojekten auf drei Arten zugeordnet werden:

-   **Akontorechnungsstellung** – Für Aufwands- und Festpreisprojekte können Akontorechnungen gestellt werden. Dabei sind für die beiden Projekttypen zwei unterschiedliche Akontoeinstellungen (jeweils eins für einen Projekttyp) erforderlich.
-   **Rechnungsstellung im periodischen Bereich** – Über die periodischen Funktionen können Buchungen projektübergreifend fakturiert werden. Die periodischen Funktionen bieten einen Überblick über die zu fakturierenden Buchungen.
-   **Mit Gutschriften bei der Rechnungsstellung** – Eine Gutschrift kann sowohl für Aufwands- als auch Festpreisprojekte erstellt werden.

## <a name="invoice-proposals"></a>Rechnungsvorschläge
Bevor Sie eine Debitorenrechnung für ein Projekt erstellen, können Sie eine vorläufige Rechnung oder einen Rechnungsvorschlag erstellen. In einem Rechnungsvorschlag können Sie Projektbuchungen auswählen, die in eine Projektrechnung einbezogen werden soll. Sie können dann die Rechnungsdetails prüfen, bevor Sie die Projektrechnung buchen und diese an den Debitor oder an eine andere Finanzierungsquelle senden.

### <a name="creating-invoice-proposals"></a>Rechnungsvorschläge erstellen

Sie können Rechnungsvorschläge erstellen, indem Sie eine Buchung manuell aus einer Liste verfügbarer Buchungen für ein angegebenes Projekt auswählen. Zudem können Sie Fakturierungsregeln einrichten, die angeben, wann ein Rechnungsvorschlag automatisch erstellt wird. So können Sie beispielsweise eine Fakturierungsregel erstellen, um einen Rechnungsvorschlag zu erstellen, wenn die Arbeit an einem Projekt zu 25, 50, 75 und 100 % abgeschlossen ist. 

Sie können Rechnungsvorschläge für folgende Buchungen erstellen:

-   Stunden, Ausgaben und andere Projektbuchungen
-   Beträge, die von Debitoren aus früheren Projektrechnungen einbehalten werden.
-   Gutschriften
-   Beträge, die Ihnen von einem Debitor bezahlt wurden, bevor ein Projekt gestartet wird.

> [!NOTE]
> Die Funktion **Sortieren nach Ressource in während der Erstellung eines Rechnungsvorschlags für Projekt aktivieren** ermöglicht dem Projektbuchhalter, die Projektbuchungen für die Berechnung nach Ressource zu sortieren, wenn er einen neuen Projektrechnungsvorschlag erstellt. Das Raster mit den verfügbaren Projektbuchungen enthält separate Felder für die **Ressourcen-ID** und die **Ressource**. In diesen Feldern können Sie nach Ressourcennamen filtern und sortieren. Diese Funktion ist standardmäßig deaktiviert. Sie kann über die Seite **Funktionsverwaltung** aktiviert werden (**Arbeitsbereiche > Funktionsverwaltung**). Bitten Sie Ihren Systemadministrator um Unterstützung, um diese Funktion zu aktivieren.

Sie können Gebührenbuchungen in einem Rechnungsvorschlag erstellen. Sie können den Verkaufspreis in Stunden-, Ausgaben-, Artikel- und Gebührenbuchungen auch ändern. Wenn Sie einen Rechnungsvorschlag buchen, werden die aktualisierten Preise und die Buchungen in den Projektberichten und der Buchungshistorie hinzugefügt. 

Um mehrere Debitorenrechnungen für ein Projekt zu erstellen, müssen Sie einen Rechnungsvorschlag für jede Rechnung erstellen. Zum Beispiel können Sie Rechnungen auf Basis der Buchungsart erstellen. Wenn Sie in einer Debitorenrechnung Stunden und in einer anderen Rechnung Artikel angeben möchten, müssen Sie separate Rechnungsvorschläge für Stundenbuchungen und für Gebührenbuchungen erstellen. 

Für ein Projekt, das mehrere Finanzierungsquellen hat, können Sie für jede Finanzierungsquelle einen separaten Rechnungsvorschlag erstellen. Auf der Seite **Zuweisungen der Finanzierungsregel** können Sie den Prozentsatz des Buchungsbetrags festlegen und jeder Finanzierungsquelle zuweisen, sowie die Quelle definieren, um Rundungsdifferenzen zu buchen.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Erstellen von Debitorenrechnungen aus Rechnungsvorschlägen

Wenn Sie einen Rechnungsvorschlag gebucht haben, wird eine Debitorenrechnung automatisch für die Buchungen erstellt, die in den Rechnungsvorschlag einbezogen sind. 

Bevor Sie einen Rechnungsvorschlag buchen, können Sie können Transaktionen hinzufügen oder löschen. So können Sie Ausgabenbuchungen entfernen, die in einem Projekt gebucht wurden, die jedoch noch nicht dem Debitor fakturierbar sind. 

Wenn es für Ihre Organisation erforderlich ist, dass Rechnungsvorschläge vor der Buchung geprüft werden, müssen Sie ihn möglicherweise über den „Projektrechnungsvorschläge prüfen“-Workflow genehmigen, bevor er gebucht wird.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Zuschussinformationen in den Seiten mit den Projektrechnungslisten anzeigen

Benutzer des öffentlichen Sektors können die **Zuschuss-ID** und den **Zuschussnamen** den **Projektrechnungsvorschlägen** und den Seiten mit den **Projektrechnung** slisten hinzufügen. Diese Spalten werden mit der Funktion **Zuschussinformationen in den Seiten mit den Projektrechnungslisten hinzufügen** aktiviert. Diese Funktion ist standardmäßig deaktiviert und kann in **Arbeitsbereiche > Funktionsverwaltung** aktiviert werden. Bitten Sie Ihren Systemadministrator um Unterstützung, um diese Funktion zu aktivieren.

## <a name="on-account-invoicing"></a>Akonto-Rechnungsstellung
Der Betrag, den Sie für ein Projekt in eine Akontorechnung eingeben, basiert auf dem Zeitpunkt, dem Vollendungsgrad in Prozent und anderen Bedingungen, die im zugehörigen Projektvertrag angegeben wurden. Der Betrag wird nicht auf Basis der Stunden, der Artikel, Ausgaben oder Gebühren berechnet, die in einem Projekt gebucht werden. 

Sie müssen zuerst eine Kontobuchung für ein Aufwandsprojekt oder ein Festpreisprojekt erstellen, bevor Sie diese Kontobuchung einer Projektrechnung hinzufügen können. In der Akontobuchung geben Sie den Betrag ein, der einem Debitor in Rechnung gestellt wird. Um eine Projektrechnung über den Betrag zu erstellen, erstellen Sie eine vorläufige Rechnung (Rechnungsvorschlag). Wählen Sie im Rechnungsvorschlag die Akontobuchung. Sie können die Kontoinformationen in dem Rechnungsvorschlag überprüfen, bevor Sie eine Projektrechnung für diesen erstellen. 

### <a name="fixed-price-projects"></a>Festpreisprojekte
Bei Festpreisprojekten basieren Akontobuchungen auf einem vereinbarten Meilenstein, Liefereinheit oder Abrechnung nach Arbeitsstatuss, wie in einem Projektvertrag angegeben. Für jede Zahlung wird eine Position erstellt, die der Projektdebitor erhalten muss. Es sind keine Abzüge erforderlich.

### <a name="time-and-material-projects"></a>Aufwandsprojekte

Für Aufwandsprojekte können Sie einem Debitor oder einer anderen Finanzierungsquelle einen Vorauszahlungsbetrag berechnen, indem Sie einen Akontorechnungsvorschlag verwenden. Geben Sie Akontobuchungen als eine Position ein. Optional können Sie zusätzliche Positionen als Abzüge eingeben, um alle Vorauszahlungen auszugleichen, die der Debitor bereits geleistet hat. Um Abzugspositionen zu erstellen, geben Sie vor dem Betrag ein Minuszeichen ein.

## <a name="invoice-control"></a>Rechnungskontrolle
Mithilfe der Rechnungskontrolle können sowohl fakturierte als auch nicht fakturierte Transaktionen nachverfolgen und Transaktionen anhand von Angeboten analysieren, um eine End-to-End-Übersicht über die Projekte, von der Angebotsphase bis zum Abschluss, anzuzeigen. Sie können sehen, welche Transaktionen einem bestimmten Projekt berechnet wurden und welche Positionen fakturiert wurden. Darüber hinaus können Sie einzelne Buchungen anzeigen, um diese nach dem Buchen anzupassen.

## <a name="invoicing-fixed-price-projects"></a>Festpreisprojekte fakturieren
Um ein Festpreisprojekt zu fakturieren, müssen Sie einen Fakturierungsplan definieren und das Fakturierungsverfahren abschließen.

### <a name="billing-schedule"></a>Fakturierungsplan

Festpreisprojekte können anhand eines Fakturierungsplans abgerechnet werden. Die Definition des Fakturierungsplans richtet sich nach einem oder mehreren Projektmeilensteinen. Für jeden Meilenstein können Sie ein bestimmtes Datum, eine Verkaufswährung, einen Verkaufspreis und eine Aktivität definieren. 

Sie können beispielweise folgenden Fakturierungsplan einrichten:

-   20 % bei Unterzeichnung des Projektvertrags
-   30 % bei der ersten Lieferung
-   15 % bei der zweiten Lieferung
-   35 % bei der letzten Lieferung

### <a name="invoicing-procedure"></a>Fakturierungsverfahren

Wenden Sie das Verfahren für die Fakturierung von Kontobeträgen an, wenn die Zwischenzahlungen zur Fakturierung bereit sind.

## <a name="vendor-invoicing"></a>Kreditorenrechnungsstellung
Wenn Sie einen Artikel von einem Kreditor bestellen und den Artikel einem Projekt zuweisen, bestimmt der Abrechnungscode, den Sie für die Bestellposition dieses Artikel auswählen, ob der eingekaufte Artikel einem Debitor in Rechnung gestellt wird. Wenn Sie Standardpositionseigenschaften einrichten, werden diese für den Artikel auf der Bestellposition angezeigt (**Positionsdetails > Projekt > Posititionsbetrag**). Es gibt zwei Möglichkeiten, um den Abrechnungscode zu ändern:

-   Stellen Sie dem Kunden des Projekts den Artikel in Rechnung. Legen Sie dazu in der Bestellung den Abrechnungscode für den Artikel auf einen fakturierbaren Wert fest und stellen Sie dann eine Rechnung an den Debitor, indem Sie die korrekte Rechnungsstellungsmethode anwenden.
-   Stellen Sie nicht dem Kunden des Projekts den Artikel in Rechnung. Wählen Sie dazu nicht den Abrechnungscode **Fakturierbar** in der Bestellposition für den Artikel. Sie können dann die Bestellung fakturieren, und es sind keine weiteren Schritte erforderlich.

> [!NOTE] 
> Freigabe-Einbehaltungspositionen sind standardmäßig nicht kostenpflichtig. Dies bedeutet, dass die Möglichkeit, einen Rechnungsvorschlag für den freigegebenen einbehaltenten Betrag zu erstellen, nicht aktiviert ist.

## <a name="credit-notes"></a>Gutschriften
Ist auf einer Debitorenrechnung ein negativer Betrag vorhanden, wird die Rechnung als Gutschrift klassifiziert. Beim Drucken erhält das Dokument die Bezeichnung "Gutschrift". 

Wird eine Gutschrift erstellt, um einen Betrag gutzuschreiben, der zuvor in Rechnung gestellt wurde, muss zunächst der fakturierte Betrag ausgewählt werden, für den die Gutschrift erstellt werden soll. Erstellen Sie anschließend die Gutschrift gemäß dem Verfahren, das auch zum Erstellen einer normalen Debitorenrechnung verwendet wird. Sie müssen die Transaktionen auswählen, die zuvor auf einer Debitorenrechnung verbucht wurden, und anschließend einen Gutschriftvorschlag erstellen und buchen. 

Das selbe Dokument kann Transaktionen, die für Gutschriften, Kreditbuchungen und bereits gebuchte Transaktionen ausgewählt sind, enthalten. Das Dokument wird entweder als Rechnung oder Gutschrift klassifiziert, abhängig davon, ob ein positiver oder negativer Gesamtbetrag vorliegt. 

Wird ein Betrag gutgeschrieben, muss zunächst der fakturierte Betrag ausgewählt werden, für den die Gutschrift erstellt werden soll und dann die Gutschrift erstellt werden. Gehen Sie zum Erstellen der Gutschrift gemäß dem Verfahren vor, das auch zum Generieren einer Debitorenrechnung verwendet wird. 

Sie können eine Rechnung mit einem negativen Betrag erstellen; die dann eine als Gutschrift klassifizierte Rechnung ist. Um eine Gutschrift zu erstellen und zu drucken, müssen Sie die Transaktionen auswählen, die zuvor in Rechnung gestellt wurden und diese Transaktionen dann bearbeiten. Augenommen bei juristischen Personen, deren primäre Adresse sich in Deutschland befindet, ist der Titel der Rechnung "Rechnungskorrektur".





[!INCLUDE[footer-include](../../includes/footer-banner.md)]