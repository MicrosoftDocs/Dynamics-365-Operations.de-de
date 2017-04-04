---
title: Vertrieb und Marketing
description: "Im Vertriebs- und Marketingmodul können verschiedene Arten von Daten im Verkaufsablauf abgerufen, gespeichert und verwendet werden. Zu diesen Daten zählen die ursprüngliche Vertriebsinitiative, künftige Weiterverfolgungsaktivitäten und zusätzliche Verkäufe."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f9e79b5dad120e057193b97d9c87665c54fea023
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-marketing"></a>Vertrieb und Marketing

Im Vertriebs- und Marketingmodul können verschiedene Arten von Daten im Verkaufsablauf abgerufen, gespeichert und verwendet werden. Zu diesen Daten zählen die ursprüngliche Vertriebsinitiative, künftige Weiterverfolgungsaktivitäten und zusätzliche Verkäufe.

<a name="marketing"></a>Marketing
---------

Marketingkampagnen und -aktivitäten dienen der Suche und dem Aufbau von Beziehungen mit potenziellen Kunden, sodass sich Erstkontakte zu Geschäftsbeziehungen entwickeln können. Im folgenden Ablaufdiagramm werden die Geschäftsprozesse für das Marketing dargestellt. [![Geschäftsprozess für Marketing] ". /media/marketing01.jpg)]". /media/marketing01.jpg)

### <a name="relationships"></a>Beziehungen

In Vertrieb und Marketing können die Erstkontakte mit potenziellen Kunden in unterschiedlichen Situationen auftreten. Beispielsweise entdecken Sie einen künftigen Kunden bei einem Messebesuch oder einen potentiellen Kunden nachdem Ihre Organisation eine Massenmail-Kampagne ausgeführt hat. Es ist sehr wichtig, dass Sie den Fluss der Entität einer Partei überblicken bevor diese Partei ein Kunde wird. Die folgende Grafik zeigt den Verlauf der Entitätsbeziehungen vom potenziellen Kunden zum Kunden. ![SalesandMarketing01 ([]. /media/salesandmarketing01.jpg)]". /media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampagnen

Eine Kampagne wird auf die Kontakte für Interessenten, potenzielle Kunden, Verkaufschancen und Debitoren ausgerichtet, die als Kampagnenteilnehmer ausgewählt wurden. In Microsoft Dynamics 365 für Arbeitsgänge, können Sie unterschiedliche Arten Kampagnen, wie das Mailing, und E-Mail-Kampagnen erstellen, das Debitorenpotential zu maximieren. Wenn Ihre Kampagne fortschreitet und Sie positive Antworten erhalten, können Sie mit dem Verkaufsprozess bei den Empfängern beginnen, die positiv auf die Kampagne reagiert haben.

## <a name="sales"></a>Vertrieb
Die Verkaufsfunktionalität wird verwendet, um Angebote zu erstellen, den weiteren und ergänzenden Verkauf an neue und vorhandene Kunden durchzuführen und um Aufträge und Rechnungen für Kunden zu erstellen. Im folgenden Ablaufdiagramm werden die Geschäftsprozesse für den Verkauf dargestellt. [![Geschäftsprozess für Vertrieb] ". /media/sales01.jpg)]". /media/sales01.jpg)

### <a name="sales-quotations"></a>Verkaufsangebote

Sie erstellen Verkaufsangebote, um Kunden ein Angebot der Waren oder Dienstleistungen zu präsentieren, die Sie bereitstellen. Kunde fordert möglichweise ein Angebot an, oder Sie erstellen ein Angebot auf eine Anforderung eines potenziellen oder bereits vorhandenen Kunden. Wenn der Kunde das Verkaufsangebot genehmigt, können Sie es in einen Auftrag konvertieren.

### <a name="up-sellcross-sell"></a>Weiterer/ergänzender Verkauf

Querverkauf und Weiterverkauf sind Techniken, Produkte zu verkaufen, wenn ein Auftrag für einen Debitoren eingegeben wird. Beim Weiterverkauf wird ein anderes Produkt anstelle des aktuellen Produkts empfohlen. Beim Querverkauf wird ein Produkt zusätzlich zum aktuellen Produkt empfohlen. Wenn Sie Produktlisten einrichten, können Sie bestimmte Regeln erstellen, um anzugeben, wann ein Produkt als Kreuzverkauf oder Obenverkaufsprodukt vorgeschlagen werden soll.

### <a name="sales-orders"></a>Aufträge

Wenn Sie einen neuen Auftrag erstellen, muss der entsprechende Auftragstyp angegeben werden. Sie haben fünf Optionen. **Hinweis:** Nach der Erstellung eines Auftrags kann jeder Auftragstyp geändert werden, mit Ausnahme des **Artikelbedarf**-Typs, wenn der Auftrag den Status **Geliefert** hat.

| Auftragstyp  | Beschreibung                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erfassung           | Verwenden Sie diesen Typ als Entwurf für einen Auftrag. Dieser Typ hat keinen Einfluss auf die Lagermengen und erzeugt keine Artikelbuchungen.                                                                                                                                                                    |
| Dauerauftrag      | Verwenden Sie diesen Typ für wiederkehrende Aufträge. Wenn der Auftrag fakturiert wird, wird der Auftragsstatus automatisch auf offen gesetzt. Die fakturierte, gelieferte Menge und die verbleibenden Lieferungen werden aktualisiert. Sie können diesen Auftragstyp nicht verwenden, wenn Sie die Lagerortverwaltungsfunktion verwenden. |
| Auftrag       | Verwenden Sie diesen Typ, wenn ein Kunde eine Bestellung erteilt oder bestätigt hat.                                                                                                                                                                                                                                        |
| Zurückgegebener Auftrag    | Verwenden Sie diesen Typ, wenn der Debitor Artikel zurückgibt. Es wird automatisch eine Rücksendungsnummer (RMA-Nummer) zugewiesen.                                                                                                                                                                                            |
| Artikelbedarf | Dieser Typ wird automatisch erstellt, wenn Sie einen Artikelverkauf durch ein Projekt vornehmen.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Kaufverträge

Durch einen Kaufvertrag verpflichtet sich der Debitor, ein Produkt in einer bestimmten Menge oder für einen bestimmten Preis über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Sonderpreise und Rabatte zustehen. Die Preise und Rabatte des Kaufvertrags setzen alle Preise und Rabatte außer Kraft, die in sämtlichen vorhandenen Handelsvereinbarungen angegeben sind. Ein Kaufvertrag ist über einen festgelegten Zeitraum gültig. Das angeforderte Lieferdatum, das für den Verkauf auf Seite **Auftrag** angegeben ist, sollte im den Gültigkeitszeitraum liegen. Standardmäßig ist der Kaufvertrag gesperrt. Bestellungen per Kaufvertrag sind nur möglich, wenn für den Vertrag der Status **Effektiv** festgelegt wurde.

### <a name="backorders"></a>Rückstände

Beim Eingeben und Überprüfen von Aufträgen müssen unter Umständen Rückstände und Ausnahmen verwaltet werden, bevor der Verkauf ausgeführt werden kann. Rückstände sind entweder Bestellungen, die von einem Lieferanten noch nicht geliefert wurden, oder Aufträge, die noch nicht an einen Kunden ausgeliefert wurden. Es ist wichtig, Rückstände zu verfolgen. Wenn sich z. B. Warenlieferungen eines Lieferanten verzögern, müssen Sie möglicherweise das Lieferdatum für einen Kunden ändern und den Kunden über die Verzögerung informieren. Rückstände können nach Artikel, Debitor oder Kreditor angezeigt werden.

#### <a name="viewing-backorders-by-item"></a>Anzeigen von Rückständen nach Artikeln

Werden Rückstände nach Artikeln angezeigt, kann der erwartete zukünftige Fluss von Buchungen im Hinblick auf einen bestimmten Artikel verfolgt werden. Beispielsweise können Sie die folgenden Informationen prüfen:

-   Die Anzahl der Aufträge, die für einen Artikel erteilt wurden.
-   Ob Lieferungen von Artikeln von Lieferanten immer noch fehlen.
-   Ob mehr Artikel bestellt werden müssen, damit alle Aufträge rechtzeitig geliefert werden können.

Durch diese Prüfung können Sie auf Kundenanfragen über den Zeitpunkt der Artikellieferung reagieren. Daneben können Sie Auftragsrückstände mit Prioritäten versehen und die Artikel, die auf Lager sind, auf die Aufträge verteilen.

#### <a name="viewing-backorders-by-customer"></a>Anzeigen von Rückständen nach Debitor

Der Überblick über Rückstände nach Kunde bietet die Möglichkeit, den Status von noch ausstehenden Kundenaufträgen anzuzeigen. Diese Prüfung ist nützlich, wenn Sie Kunden antworten müssen, die auf ihre verzögerten Artikel warten.

#### <a name="viewing-backorders-by-vendor"></a>Anzeigen von Rückständen nach Kreditoren

Der Überblick über Rückstände nach Kreditoren ist hilfreich, um fehlende Lieferungen zu verfolgen und um erwartete Lieferzeiten anzuzeigen. Diese Prüfung ist auch nützlich beim Priorisieren von Rückständen, wenn Produkte von Lieferanten eintreffen und Aufträge zur Lieferung ausgewählt werden müssen.

### <a name="invoices"></a>Rechnungen

Sie können drei Arten von Rechnungen während des Verkaufsprozesses erstellen:

-   Debitorenrechnung
-   Freitextrechnung
-   Proforma-Rechnung

#### <a name="customer-invoice"></a>Debitorenrechnung

Bei einer Debitorenrechnung handelt es sich um eine Rechnung, die ein Debitor im Zusammenhang mit einem Verkauf von einer Organisation erhält. Die Erstellung dieser Art von Debitorenrechnung erfolgt auf Basis eines Auftrags, in dem eine Kopfzeile und eine oder mehrere Positionen für Artikel oder Dienstleistungen enthalten sind. Mit der Debitorenrechnung wird der Zyklus aus Auftrag, Lieferschein und Rechnung abgeschlossen.  

Sie können eine einzelne Debitorenrechnung, basierend auf einem Auftrag oder dem Lieferschein und Datum, buchen und drucken. Sie können auch mehrere Debitorenrechnungen gleichzeitig, basierend auf den Lieferscheinen und dem Datum, buchen und drucken. Durch Buchen einer einzelnen Rechnung anhand eines Auftrags, wird die Menge für den **Rechnungsrestbetrag** mit der Summe der fakturierten Mengen aus dem ausgewählten Auftrag aktualisiert.  

Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Aufrags gleich 0 (Null) ist, wird der Status des Auftrags zu **In Rechnung gestellt** geändert. Ist die Menge in einem der Felder nicht Null ist, bleibt der Status des Auftrags unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden. Wenn Sie eine oder mehrere Debitorenrechnungen, basierend auf den Lieferscheinen, buchen und drucken möchten, müssen Sie bereits mindestens einen Lieferschein für jeden Auftrag gebucht haben. Die Debitorenrechnung basiert auf den Lieferscheinen und enthält die auf den Lieferscheinen angegebenen Mengen.  

Sie können basierend auf den bisher versendeten Artikeln der Lieferscheinpositionen eine Debitorenrechnung erstellen, auch wenn noch nicht alle Artikel eines bestimmten Auftrags versendet wurden. Das kann der Fall sein, wenn Ihre juristische Person monatlich eine Rechnung pro Debitor für alle Lieferungen ausstellt, die während des Monats versendet wurden. Jeder Lieferschein stellt eine teilweise oder vollständig abgeschlossene Artikellieferung für einen Auftrag dar.  

Durch Buchen der Rechnung wird die Menge des **Rechnungsrestbetrags** für jeden Artikel mit der Summe der gelieferten Mengen aus den ausgewählten Lieferscheinen aktualisiert. Wenn die Menge für den **Rechnungsrestbetrag** und die Menge **Rest liefern** für alle Artikel des Aufrags gleich 0 (Null) ist, wird der Status des Auftrags zu **In Rechnung gestellt** geändert. Ist die Menge nicht Null, bleibt der Status des Auftrags unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden. Die Lagerbuchungen werden mit der Rechnungsnummer aktualisiert, und der Status in der Auftragsposition wird auf **In Rechnung gestellt** geändert.

#### <a name="free-text-invoice"></a>Freitextrechnung

Eine Freitextrechnung ist eine Rechnung, die keinem Auftrag zugeordnet ist. Sie enthält Auftragspositionen mit Sachkonten, Freitextbeschreibungen und Verkaufsbeträgen. Auf dieser Art von Rechnung können Sie keine Artikelnummer eingeben und müssen die geeigneten Mehrwertsteuerinformationen hinzufügen. Ein Hauptkonto für den Verkauf wird für jede Rechnungsposition angegeben. Der Debitorensaldo wird auf das Summenkonto aus dem Buchungsprofil gebucht, das für die Freitextrechnung verwendet wird.

#### <a name="pro-forma-invoice"></a>Proforma-Rechnung

Bei einer Proforma-Rechnung handelt es sich um eine Rechnung, die vor dem Buchen der Rechnung als Vorkalkulation der tatsächlichen Rechnungsbeträge vorbereitet wird. Proforma-Rechnungen können sowohl für Debitoren- als auch für Freitextrechnungen gedruckt werden.


