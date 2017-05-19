---
title: "Beschaffungsübersicht"
description: "Dieser Artikel enthält eine Übersicht der Funktionen, die im Beschaffungsmodul verfügbar sind."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: e8a12f846bb24c9fc79c3533d4e65a2d3ece257b
ms.openlocfilehash: 6d4d476e294e1b5cbe91a61a7ffe151a6c865ea6
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2017


---

# <a name="procurement-and-sourcing-overview"></a>Beschaffungsübersicht

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält eine Übersicht der Funktionen, die im Beschaffungsmodul verfügbar sind.

Die Beschaffung umfasst alle Schritte von der Identifikation einer Anforderung für Produkte und Dienste bis zur Beschaffung des Produkts, des Eingangs, der Fakturierung und der Verarbeitung der Zahlung mit Kreditoren. Beschaffungsprozesse können für bestimmte Geschäftsanforderungen konfiguriert werden, indem Einkaufsrichtlinien und Workflows definiert werden.

## <a name="identifying-a-need-for-product-and-services"></a>Identifizieren einer Anforderung für Produkte und Dienste
Der Bedarf für Produkte oder Dienste entsteht möglicherweise aus *Anforderungen*, beispielsweise wenn ein Mitarbeiter ein Produkt benötigt. *Produktkataloge *können so eingerichtet werden, dass die Auswahl der verfügbaren Produkte, aus denen Sie auswählen, geführt wird, oder dass Produkte angefodert werden können, die noch nicht in einem Katalog bereitgestellt werden, wodurch die Einkaufsabteilung entscheiden kann, wie das Produkt beschafft werden kann.  

*Ausgabenlimits *können verwendet werden, um die Ausgaben für Materialanforderungen einzuschränken, und der *Einkaufsworkflow *fügt die Option des Benötigens einer Genehmigung hinzu, bevor Sie bestellen. Es ist auch möglich, Budgetmittelzuteilung anzugeben, falls erforderlich.  
  
Die Beschaffungsabteilung identifiziert Lieferanten für erforderliche Produkte und Dienste, und dies kann bedeuten, dass eine *Angebotsanforderung *an mehrere mögliche Lieferanten gesendet wird. Es ist möglich, die Angaben des Produkts, das angefordert wird, freizugeben, und potenzieller Kreditoren können diese Angaben sehen, um festzustellen, ob sie ein Produkt liefern können, das ihnen entspricht. Kreditoren machen dann Angebote, die durch die Beschaffungsabteilung geprüft werden, bevor der Lieferant ausgewählt wird, von dem sie beschaffen möchten.  

Bestellungen beinhalten eine Option zum Senden einer *Einkaufsabfrage *an den Kreditor als Alternative zu einem umfassenderen Angebotsanforderungsprozess. Die Einkaufabfrage kann verwendet werden, um Bedingungen, wie Preise, Rabatte und Lieferdatum, für den Auftrag einzurichten. Wenn Kreditoren so eingerichtet werden, dass sie das Portal **Kreditor** verwenden können, ist die Funktion Einkaufsabfrage deaktiviert. Stattdessen wird der Auftrag im Portal**Kreditor** freigegeben, und wenn eine *Bestätigungsanforderung* gesendet wird, kann der Kreditor den Auftrag direkt bestätigen.  

*Lieferantenkataloge *können verwendet werden, um Informationen zum Produktsortiment zu sammeln, das Kreditoren bereitstellen können. Kreditoren können eigene Katalog veröffentlichen, sodass es einfacher ist, den Katalog aktuell zu halten. Es ist möglich, einem Produkt eine *Liste genehmigter Kreditoren* hinzuzufügen. Dies kann bei der Kreditorenauswahl helfen, wenn neue Bestellungen geöffnet werden, und verhindern, dass nicht erwünschte Kreditoren verwendet werden.

## <a name="procurement"></a>Beschaffung
*Bestellungen *können auf mehrere unterschiedliche Arten erstellt werden, einschließlich:

-   Als Ergebnis der Produktprogrammplanung, die einen Bedarf identifiziert ist, der einen Einkauf erforderlich. Bei diesem Prozess werden Artikelbuchungen generiert geplante Einkaufsbestellungen und wenn diese freigegeben werden, werden Bestellungen erzeugt.
-   Durch das Verarbeiten von Bestellanforderungen, die in Beschaffung resultieren.
-   Durch das Verarbeiten von Kaufverträgen, in denen Bestellungen als freigegebene Aufträge aus den Vereinbarungen erstellt werden. Dies wird häufig verwendet, wenn Kaufverträge verwendet werden, um Abrufaufträge darzustellen.
-   Manuell, wenn die Bestellung, die erstellt wird, nicht auf einem anderen Dokument basiert.

Bestellungen, die mit *Einkaufgenehmigungsworkflows* konfiguriert werden, müssen genehmigt werden, bevor sie als genehmigt registriert werden. Dies ist erforderlich, bevor der Auftrag weiter verarbeitet werden kann.  

Bestellungen sind *bestätigt*, um darzustellen, dass eine Vereinbarung mit dem Kreditor ausgehandelt wurde. Die Bestellung durchläuft dann verschiedene Status, bis sie schließlich in Rechnung gestellt oder storniert wird.  

Wenn Sie eine Bestellung erstellen, werden viele der Felder mit Werten vorausgefüllt, die aus den Informationen stammen, die zum Kreditor auf der Seite **Kreditoren**gespeichert sind. Das bedeutet, dass es eine begrenzte Anzahl an Feldern gibt, die Sie in der Bestellung ausfüllen müssen, obwohl Sie entscheiden können, die Standardwerte zu überschreiben.

### <a name="prices-and-discounts"></a>Preise und Rabatte

Preise und Rabatte umfassen Informationen zu Preisen, Rabatten und Rückvergütungsbedingungen, die sie anbieten. Preise und Rabatte können als *Handels**vereinbarungen* dargestellt werden. Handelsvereinbarungen stellen Kreditorenpreislisten mit Preisen oder Rabatte dar und haben einen bestimmten Satz an Daten, für die Vereinbarung gilt. Preise und Rabatte können durch *Kaufverträge *verhandelt und repräsentiert werden, mit Bedingungen, wie Zusagen, bestimmte Volumen zu kaufen, oder Geldbeträge als Vorbedingung für die vereinbarten Bedingungen. *Rückvergütungsvereinbarungen *können mit Kreditoren erstellt werden, wenn die Beschaffung von bestimmten Produkten oder Gruppen einen Rabatt vom Kreditor auslösen können, je nach Einkaufsbetrag oder Volumen.

### <a name="delivery-options"></a>Lieferoptionen

Es gibt verschiedene Optionen für den Versandprozess, der einer Bestellung zugeordnet ist. Bestellte Produkte können in *Lieferzeitpläne* aufgeteilt werden, wobei Teile der bestellten Menge für die Lieferung an unterschiedliche Daten geplant werden können. Die Lieferung kann auch eine *Direktlieferung* enthalten, die aus einem Auftrag initiiert wird, wodurch die Generierung des Lieferscheins auf dem Auftrag zur gleichen Zeit automatisiert wird, wie der Produktzugang auf der Bestellung erfasst wird. Bestellungen können Teil einer *Intercompany-Auftragskette *sein, die auch als Intercompany-Bestellungen bezeichnet werden, in denen Produkte aus einem passenden Intercompany-Auftrag bestellt werden. In diesem Fall sind einige Schritte zwischen zwei verwandten Intercompany-Aufträgen automatisiert.

### <a name="supplementary-items"></a>Zusätzliche Artikel

Produkte können so eingerichtet werden, dass *zusätzliche Artikel* enthalten sein können. Dies dient dem Zweck, Produkte vorzuschlagen, die mit dem Produkt verbunden sind, das bestellt wurde. Die zusätzlichen Produkte sind möglicherweise erforderlich oder auch optional. In einigen Fällen werden zusätzliche Artikel möglicherweise als kostenlose Produkte zum Kauf anderer Produkte hinzugefügt.

### <a name="purchase-order-charges"></a>Belastungen der Bestellung

Belastungen können einer Bestellung zugeordnet werden. Dies kann durch die Einrichtung automatischer Belastungen automatisch geschehen oder indem Sie die Belastungen manuell hinzufügen. Belastungen können dem Auftrag auf Kopfzeilenebene oder auf Auftragspositionsebene zugeordnet werden. Die Belastungsaufstellung kann auf unterschiedliche Arten eingerichtet werden. Sie können beispielsweise eine Belastung einrichten, die als Produktkosten verbucht wird. Wenn Sie dies tun, müssen die Belastungen auf Auftragspositionsebene zugeordnet werden, bevor der Auftrag bestätigt werden kann. Es gibt eine Option, die helfen kann, Belastungen aus der Auftragskopfzeile zu den Positionen zuzuweisen.

## <a name="product-receipt-and-invoicing"></a>Produktzugang und Rechnungsstellung
Für Bestellungen, die physische Produkte enthalten, muss in der Regel eine *Eingangsregistrierung* innerhalb eines Lagerorts vorgenommen werden. Anschließend wird ein *Produktzugang *für den Auftrag erfasst. Bestellungen mit Produkten, die den Anforderungen entsprechen, werden möglicherweise so konfiguriert, dass der Mitarbeiter, der die Produkte angefordert hat, auch eine *Empfangsbestätigung* vorlegen muss.  

Einige Bestellungen enthalten Produkte, die Dienste oder andere nichtphysische Produkte sind, für die keine Bestätigung im Lagerort benötigt wird. Produkte können als Dienste oder *Beschaffungskategorien *direkt auf der Bestellung für solche Aufträge verwendet werden. Bei diesen Bestellungen wird die Buchung des Produktzugangs manchmal übersprungen und die Bestellung wird direkt fakturiert, oder alternativ erfolgt die Produktzugangsregistrierung auf der Bestellung ohne eine vorherige Eingangsregistrierung.  

Der Produktempfang kann in der Soll=Istrückmeldung für einen bestimmten Zweck resultieren. Hierzu zählen der implizite Verbrauch mit Direktlieferung, der Verbrauch in Richtung eines Projekts oder die Berechnung des Produkts als Anlage.  

Wenn * Kreditorenrechnungen* vom Kreditor eingegangen sind, werden sie zuerst im *Rechnungsbuch *unabhängig von der Bestellung erfasst und später als Datensatz für die Bestellung genehmigt. Das Erfassen der Kreditorenrechnung mit der Bestellung umfasst den Abgleich des Produktzugangs mit der Rechnung.  

*Buchhaltungsverteilungen* können auf der Bestellung angegeben werden, um zu beschreiben, wie die Berechnung innerhalb des Sachkontos erfolgen soll, und können auch festlegen, wie die Budgetmittelzuteilung erfolgt, sofern diese in Ihrer Konfiguration enthalten ist.  

Fakturierte Bestellungen erfassen die Verbindlichkeiten im Kreditorenkonto innerhalb der Kreditoren, von wo aus die *K*reditoren*zahlung *verarbeitet werden kann.

## <a name="vendor-performance"></a>Kreditorleistung
Leistung und Prüfung des Einkaufs wird unterstützt durch *Beschaffungs- und Kreditorenberichte,* die eine Ausgabenanalyse und Kreditorenleistungsanalyse enthalten.




