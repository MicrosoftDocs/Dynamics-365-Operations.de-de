---
title: Dreiseitige Abgleichsrichtlinien
description: "Dieser Artikel enthält Beispiele für den dreiseitigen Abgleich."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4e9ee51394ee7c1663de2396131fa36a3fa17f7d
ms.openlocfilehash: d9d105ea6a91c53c3d45feedb8ea3ba81983f926
ms.lasthandoff: 03/31/2017


---

# <a name="three-way-matching-policies"></a>Dreiseitige Abgleichsrichtlinien

Dieser Artikel enthält Beispiele für den dreiseitigen Abgleich.

<a name="example-three-way-matching-for-items"></a>Beispiel: Dreiseitiger Abgleich für Artikel
-------------------------------------

**Zusammenfassung:** Kurt ist Controller in der Unternehmenszentrale einer juristischen Person mit dem Namen Fabrikam. Kurt beschließt, dass alle Kreditorenrechnungen, die auf Bestellungen beruhen, mit Bestellpositionen abgeglichen werden sollen (zweiseitiger Abgleich). Beim Einkauf von Artikeln, die als Anlagen verwendet werden, müssen die Rechnungen sowohl mit den Bestellpositionen als auch mit den Produktzugangspositionen abgeglichen werden (dreiseitiger Abgleich).

Fabrikam arbeitet mit mehreren juristischen Personen und Mitarbeitern in allen Teilen der Welt. Mit zunehmendem Buchungsvolumen nehmen auch die Abweichungen zwischen Zugängen und Rechnungen zu. Dies führt dazu, dass Anlagen abgeschrieben werden. Rechnungen von Kreditoren werden zwar bezahlt, der Prozess schließt jedoch keine Erfassung von Abweichungen ein, wenn weniger Artikel als bestellt eingehen oder wenn Artikel überhaupt nicht eingehen. Zudem steigen die Ausgaben, da die Mitarbeiter für ihre Arbeit weiterhin Werkzeug und andere Materialien benötigen. Kurt möchte sicherstellen, dass die Kreditoren die bestellten Produkte versenden und dass die Fabrikam-Mitarbeiter die Artikel erhalten. Daher benötigt Kurt einen zweiseitigen und dreiseitigen Abgleich für alle juristischen Personen der Organisation. Mit dem Rechnungsabgleich lässt sich sicherstellen, dass Probleme mit verschwundenen oder nicht erhaltenen Artikeln erfasst und gelöst werden können. 

Die Rechnungsabgleichsrichtlinien in diesem Beispiel unterstützen Mitarbeiter mit den folgenden Rollen, diese Ziele zu erreichen:

-   Kurt ist Controller beim Unternehmen Fabrikam. Er kann den Mitarbeitern seiner Organisation helfen, Probleme bei der Bestellung, beim Eingang und bei der Bezahlung von Artikeln (Waren und Dienstleistungen) von Kreditoren zu erkennen und zu beheben.
-   Phyllis und April sind Buchhaltungsleiterinnen in der Kreditorenabteilung der USA-Division von Fabrikam. Sie können eine Unternehmensrichtlinie erzwingen und sicherstellen, dass Rechnungen erst bezahlt werden, nachdem die Rechnungen mit der Bestellung und ggf. dem Eingang der Waren und Dienstleistungen abgeglichen wurden.
-   Tony ist Produktionsleiter der USA-Division von Fabrikam. Er und andere Produktionsmitarbeiter können sicherstellen, dass der Eingang der Artikel mit deren Bestellung bei den Kreditoren übereinstimmt und dass die Artikel erfasst werden, sodass die Mitarbeiter über die für ihre Arbeit notwendigen Dinge verfügen.

### <a name="prerequisites"></a>Voraussetzungen

-   Kurt legt die Abgleichsrichtlinie auf der Ebene der juristischen Person auf "Dreiseitiger Abgleich" fest.
-   Kurt legt die Umschaltfläche "Abgleichstatus des Kopfes automatisch aktualisieren" bei der juristischen Person auf "Ja" fest.
-   Kurt legt das Feld "Preissummen abgleichen" für die juristische Person auf "Prozentsatz" fest und gibt 15 % als Toleranzprozentsatz ein.
-   Kurt legt die Abgleichsrichtlinie auf der Artikelebene für Artikel 1500 - Maschine CNC Milicron auf "Dreiseitiger Abgleich" fest. Dieser Artikel ist ein Aktivposten, der bei Fabrikam für die Produktion verwendet wird. Rechnungen über diesen Artikel werden in Bezug auf die Preise mit Bestellpositionen und in Bezug auf die Mengen mit Produktzugängen abgeglichen.
-   Tony gibt eine Anforderung für fünf CNC Milicron-Maschinen ein. Alicia, Bestellungssekretärin bei Fabrikam, gibt eine Bestellung an eine juristische Person mit dem Namen Contoso aus, welche die Artikel liefern soll.

    | Artikelnummer                 | Menge | Preis je Einheit | Nettobetrag | Kennung der sonstigen Zuschläge        | Wert der sonstigen Zuschläge |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – Maschine CNC Milicron | 5        | 8.000,00   | 40.000,00  | Lieferung und Bearbeitung | 3.000,00      |

-   Arnie, Debitorensekretär bei Contoso, prüft die Lieferungen für die Woche. Arnie wählt Lieferungsbuchungen aus, um Fabrikam für die Lieferung der CNC Milicron-Maschinen zu fakturieren. Arnie fügt einen Zuschlag für Lieferung und Bearbeitung hinzu. Fabrikam wird betrachtet den Zuschlag als Teil der Anlagekosten.

### <a name="scenario"></a>Szenario

1.  Thomas, eine Arbeitskraft in der Empfangsabteilung bei Fabrikam, nimmt die Gesamtmenge der Maschinen in Empfang, die von Contoso geliefert werden. Er gibt auf einem Produktzugang die Menge 5 ein. Da die Bestellung vollständig eingegangen ist, ändert sich der Status der Bestellung in "Eingegangen".
2.  April, die Kreditorenkoordinatorin bei Fabrikam, gibt die von Contoso übermittelte Rechnung ein und überprüft sie. Sie prüft die folgenden Informationen:
    -   Bei Artikeln, für die ein dreiseitiger Abgleich erforderlich ist, muss die in der Rechnungsposition angegebene Menge der eingegangenen Menge entsprechen. Die eingegangene Menge wird auf dem Produktzugang angegeben, der mit der Rechnung abgeglichen wird.
    -   Für Artikel, die zweiseitigen oder dreiseitiger Abgleich erforderlich, sind die Preise auf der Rechnungsposition innerhalb der Toleranz, die in Microsoft Dynamics 365 für Operations.This enthält die folgenden Arten von Preis werden definiert werden:
        -   Nettostückpreis-Abgleich – Der Nettostückpreis der Rechnungsposition entspricht im Rahmen des Toleranzprozentsatzes dem Nettostückpreis der Bestellposition. In diesem Beispiel beträgt die Nettostückpreistoleranz +8 %.
        -   Preissummenabgleich – Der Nettobetrag der Rechnungsposition entspricht dem Nettobetrag den Bestellposition und liegt innerhalb des Toleranzprozentsatzes und/oder des Toleranzbetrags. In diesem Beispiel beträgt die Toleranz für den Preissummenabgleich +15 %.

Die Papierrechnung von Contoso enthält folgende Informationen.

| Artikel                        | Menge | Preis je Einheit | Nettobetrag |
|-----------------------------|----------|------------|------------|
| 1500 – Maschine CNC Milicron | 5        | 8.100,00   | 40.500,00  |
| Versandkostenanteil       |          |            | 4.000,00   |
| Steuerl. Buchung                         |          |            | 0,00       |
| Gesamt                       |          |            | 44.500,00  |

In Microsoft Dynamics 365 für Arbeitsgänge, enthält die Rechnungsposition die folgenden Informationen.

| Artikelnummer                 | Menge | Preis je Einheit | Nettobetrag der Position | Abgleichsrichtlinie    | Produktzugang-Mengenabgleich | Preisabgleich | Preissummenabgleich |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – Maschine CNC Milicron | 5        | 8.100,00   | 40.500,00       | Dreiseitiger Abgleich | Erfolgreich                         | Erfolgreich      | Erfolgreich            |

Da diese Position im Rechnungsabgleichsprozess bestätigt wird, kann die Rechnung gebucht werden.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a>Beispiel: Dreiseitiger Abgleich für Kombinationen von Artikeln und Kreditoren
Zusammenfassung: Kurt ist Controller in der Unternehmenszentrale einer juristischen Person mit dem Namen Fabrikam. Kurt beschließt, dass alle Rechnungen, die auf Bestellungen beruhen, mit Bestellpositionen abgeglichen werden sollen (zweiseitiger Abgleich). Cassie ist Buchhalterin bei der Malaysia-Division von Fabrikam. Sie gibt an, dass ausgewählte Artikel, die bei bestimmten Kreditoren in Malaysia bestellt werden, sowohl mit den Bestellpositionen als auch mit den Produktzugangspositionen abgeglichen werden sollen (dreiseitiger Abgleich). Bei bestimmten Bestellungen kann sie die Abgleichsrichtlinie auch mit einer höheren Abgleichsebene überschreiben. 

Das Volumen und die Beträge sind klein, und es gab Probleme mit der Lieferung einiger Kreditoren in Malaysia. Daher legt Cassie für bestimmte Kombinationen von Kreditoren und Artikeln, die in Malaysia beschafft werden, einen dreiseitigen Abgleich fest. 

Die Rechnungsabgleichsrichtlinien in diesem Beispiel unterstützen Mitarbeiter mit den folgenden Rollen, diese Ziele zu erreichen:
-   Kurt ist Controller beim Unternehmen Fabrikam. Er kann den Mitarbeitern seiner Organisation helfen, Probleme bei der Bestellung, beim Eingang und bei der Bezahlung von Artikeln (Waren und Dienstleistungen) von Kreditoren zu erkennen und zu beheben.
-   Cassie ist Buchhalterin bei der Malaysia-Division von Fabrikam. Sie kann eine Unternehmensrichtlinie erzwingen und sicherstellen, dass Rechnungen erst bezahlt werden, nachdem sie mit den Bestellpositionen und den Produkteingängen abgeglichen wurden, die den Eingang der Güter und Dienstleistungen darstellen. Sie hat außerdem die Möglichkeit, bei bestimmten Artikeln den Grad an Kontrolle auf einen dreiseitigen Abgleich heraufzustufen, um die Betriebskosten zu kontrollieren.

### <a name="prerequisites"></a>Voraussetzungen

-   Kurt legt die Abgleichsrichtlinie auf der Ebene der juristischen Person auf "Zweiseitiger Abgleich" fest.
-   Kurt legt das Feld "Preissummen abgleichen" für die juristische Person auf "Prozentsatz" fest und gibt 10 % als Toleranzprozentsatz ein.
-   Kurt legt die Stückpreistoleranz für alle Artikel auf 2 % fest.
-   Cassie legt die Abgleichsrichtlinie auf der Ebene der Kombination von Artikel und Kreditor für den Artikel PH2500 fest – Computer und Kreditor Contoso auf "Dreiseitiger Abgleich".
-   Alicia, Bestellungssekretärin in der Malaysia-Division von Fabrikam, sendet Bestellungen über die Lieferung von drei Artikeln an Contoso, wie in der folgenden Tabelle dargestellt wird. Wenn sie die Bestellung erstellt, überschreibt sie die Abgleichsrichtlinie für die drahtlose Maus, sodass ein dreiseitiger Abgleich anstelle eines zweiseitigen Abgleichs erfolgt.

    | Artikelnummer           | Menge | Preis je Einheit | Nettobetrag | Abgleichsrichtlinie (Standardeintrag) | Abgleichsrichtlinie (in der Bestellposition) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – Computer     | 2        | 2.500,00   | 5.000,00   | Dreiseitiger Abgleich              | Dreiseitiger Abgleich                           |
    | MM01 – drahtlose Maus | 2        | 40,00      | 80,00      | Zweiseitiger Abgleich                | Dreiseitiger Abgleich                           |
    | USB-Laufwerk             | 200      | 10,00      | 2.000,00   | Zweiseitiger Abgleich                | Zweiseitiger Abgleich                             |

### <a name="scenario"></a>Szenario

1.  Die Artikel treffen ein. Thomas, eine Arbeitskraft in der Empfangsabteilung der Malaysia-Division von Fabrikam, wird gestört und bucht den Produktzugang nicht sofort.
2.  April, die Kreditorenkoordinatorin bei Fabrikam, gibt die von Contoso übermittelte Rechnung ein und überprüft sie. Sie prüft die folgenden Informationen:
    -   Bei Artikeln, für die ein dreiseitiger Abgleich erforderlich ist, muss die in der Rechnungsposition angegebene Menge der eingegangenen Menge entsprechen. Die eingegangene Menge wird auf dem Produktzugang angegeben, der mit der Rechnung abgeglichen wird.
    -   Für Artikel, die zweiseitigen oder dreiseitiger Abgleich erforderlich, sind die Preise auf der Rechnungsposition innerhalb der Toleranz, die in Microsoft Dynamics 365 für Arbeitsgänge definiert werden. Dazu zählen die folgenden Preisabgleichsarten:
        -   Nettostückpreis-Abgleich – Der Nettostückpreis der Rechnungsposition entspricht im Rahmen des Toleranzprozentsatzes dem Nettostückpreis der Bestellposition. In diesem Beispiel beträgt die Nettostückpreistoleranz +2 %.
        -   Preissummenabgleich – Der Nettobetrag der Rechnungsposition entspricht dem Nettobetrag den Bestellposition und liegt innerhalb des Toleranzprozentsatzes und/oder des Toleranzbetrags. In diesem Beispiel beträgt die Toleranz für den Preissummenabgleich +10 %.

Die Papierrechnung von Contoso enthält folgende Informationen.

| Artikel                  | Menge | Preis je Einheit | Nettobetrag |
|-----------------------|----------|------------|------------|
| PH2500 – Computer     | 2        | 2.500,00   | 5.000,00   |
| MM01 – drahtlose Maus | 2        | 41,00      | 82,00      |
| USB-Laufwerk             | 200      | 10,05      | 2.010,00   |
| Gesamtrechnung         |          |            | 7.092,00   |

In Microsoft Dynamics 365 für Arbeitsgänge, enthält die Rechnungsposition die folgenden Informationen.

| Artikelnummer           | Menge | Preis je Einheit | Nettobetrag der Position | Abgleichsrichtlinie    | Produktzugang-Mengenabgleich | Preisabgleich | Preissummenabgleich |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – Computer     | 2        | 2.500,00   | 5.000,00        | Dreiseitiger Abgleich | Fehlgeschlagen                         | Erfolgreich      | Erfolgreich            |
| MM01 – drahtlose Maus | 2        | 41,00      | 82,00           | Dreiseitiger Abgleich | Fehlgeschlagen                         | Fehlgeschlagen      | Erfolgreich            |
| USB-Laufwerk             | 200      | 10,05      | 2010,00         | Zweiseitiger Abgleich   |                                | Erfolgreich      | Erfolgreich            |

Beachten Sie die folgenden Punkte:
-   Bei der Position "PH2500 – Computer" ist in der Spalte "Produktzugangsmenge" ein Warnsymbol zu sehen, da die Rechnungsposition nicht mit einem Produktzugang abgeglichen ist.
-   Bei der Position "MM01 – Drahtlose Maus" ist in der Spalte "Produktzugangsmenge" ein Warnsymbol zu sehen, da die Rechnungsposition nicht mit einem Produktzugang abgeglichen ist. Die Spalte Stückpreis-Abgleich enthält ein Warnsymbol, da die Nettostückpreis-Toleranz von 2 % überschritten wird.
-   Bei der Position "USB-Laufwerk" ist die Spalte "Produktzugang-Mengenabgleich" leer, da der zweiseitige Abgleich nicht den Mengen der Rechnungsposition und der Produktzugangsposition entspricht.

Wenn eine Genehmigung erforderlich ist, damit Rechnungen mit Abweichungen beim Rechnungsabgleich gebucht werden können, muss die Umschaltfläche "Buchungen mit beim Abgleich erkannten Abweichungen genehmigen" auf der Seite "Details zum Rechnungsabgleich" ausgewählt sein. Erst dann kann die Rechnung mit Preis- und Mengenabgleichsfehlern gebucht werden. Ist keine Genehmigung erforderlich, kann die Fakturierung fortgesetzt werden, wenn es keine weiteren Buchungsfehler gibt.


Weitere Informationen finden Sie accounts-payable-invoice-matching.md Kreditorenrechnungsabgleich []().


