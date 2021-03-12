---
title: Bericht "Berechnung der Verpackungsmaterialgebühren" für Österreich
description: Dieses Thema enthält Informationen zu Verpackungsmaterialsätze und Gebühren in Österreich.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingMaterialTransPurch
audience: Application User
ms.reviewer: kfend
ms.custom: 268034
ms.search.region: Austria
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9d0c97eda3d463a663faeeabdd11533e300528a6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978280"
---
# <a name="packing-material-fee-calculation-for-austria"></a>Bericht "Berechnung der Verpackungsmaterialgebühren" für Österreich

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu Verpackungsmaterialsätze und Gebühren in Österreich.

In Europa gibt es Verpackungsmüll-Bestimmungen. Diese Bestimmungen arbeiten mit dem Prinzip "Kollektiherstellerzuständigkeit. " Das bedeutet, sie erzwingen die Anforderung, für die der Verkäufer oder Hersteller von Verpackungen für die Umwelteinwirkung dieser Zuständigkeit für die Verpackung Verantwortung übernehmen. Entsprechend den Bestimmungen sind Hersteller dazu verpflichtet, einen Teil der Kosten und des Wiederverwendens der Beitreibung der Verpackung zu bezahlen. Diese Zahlung ist als Verpackungsmaterialgebühr bekannt<em>,</em> und wird periodisch dem Recyclingunternehmen bezahlt. Ein Unternehmen muss das Gewicht jeder Typ Verpackungsmaterial Papier (, Plastik, Metall, usw.) berechnen das während eines Verkaufs oder eines Einkaufs verwendet wurde, und das Gewicht nach dem Satz des Pakets multiplizieren. Die Regierungsbehörde stellt den Verpackungsmaterialsatz für jeden Paketmaterialtyp bereit. In Österreich wird eine komplexere Formel für Verpackungsmaterialgebühren verwendet. Verpackungsmaterialien werden in verschiedene Kategorien gruppieren (beispielsweise, Haushalt und Werbung) dividiert, und stellt für die Behörde von Verpackungsmaterialien in den einzelnen Kategorien verfügbar. Die Kategorie, in die das Verpackungsmaterial gehört, hängt von der Größe und den Produkten ab, die für die Verpackung verwendet wurde. Verpackungsmaterialgebühren werden kalkuliert und erfasst, es werden jedoch keine Sachkontobuchungen ausgeführt, da die Gebühren nicht als Steuern betrachtet werden, die an eine Behörde zu entrichten sind.

## <a name="prerequisites"></a>Voraussetzungen
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kategoriehierarchien</td>
<td>Sie müssen Kategoriehierarchien für Produkte erstellen. Für jede Kategoriehierarchie erstellen Sie Knoten, die als Produktgruppen für die Berechnung der Verpackungsmaterialgebühren verwendet werden. Sie müssen einen Kategoriehierarchietyp für Verpackungsmaterialien erstellen und die Kategoriehierarchie auf setzen. <strong>Verpackung</strong> <strong></strong> <strong>Hinweis:</strong> Sie können eine Verpackungskategoriehierarchie für nur einen Kategoriehierarchietyp einrichten. Nachdem Sie Kategoriehierarchien erstellt haben, führen Sie die folgenden Schritte aus, um ein Produkt in einer Kategoriehierarchie zuzuordnen.
<ol>
<li>Doppelklicken Sie auf der Listenseite auf ein <strong>Produkts</strong> in der Liste.</li>
<li>Klicken Sie auf der Schaltfläche <strong>Produkte</strong> auf <strong>Produktakategorien</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Verpackungsklassen</td>
<td>Erstellen oder Verwalten von Verpackungsklassen für die Berechnung der Verpackungsmaterialgebühren.</td>
</tr>
<tr class="odd">
<td>Tarifkategorien</td>
<td>Erstellen oder Verwalten von Tarifkategorien für die Berechnung der Verpackungsmaterialgebühren.</td>
</tr>
<tr class="even">
<td>Verpackungsmaterialcode</td>
<td>Erstellen Sie Verpackungsmaterialcodes für jeden Typ von Verpackungsmaterial, das definiert ist.</td>
</tr>
<tr class="odd">
<td>Verpackungsmaterialgebühren</td>
<td>Geben Sie Verpackungsmaterialgebühren für jeden Verpackungsmaterialcode an. Legen Sie für jeden Materialtyp den Gültigkeitszeitraum, die Tarifkategorie, den Preis pro Material, die Währung und die Maßeinheit fest.</td>
</tr>
<tr class="even">
<td>Verpackungsmaterialzuteilung</td>
<td>Definieren Sie, welche Materialien in einer Paketeinheit eingeschlossen sind, so dass Sie Gewichte zuzuweisen und die Anzahl der Artikel in der Verpackungseinheit addieren können. Sie können Verpackungseinheiten für einzelne Artikel, Verpackungsgruppen oder für alle Artikel festlegen. <strong>Hinweis:</strong> Wenn dem Artikel in der ausgewählten Auftragsposition eine Verpackungseinheit zugeordnet wurde, werden die Verpackungseinheit und die Verpackungsmenge automatisch geladen. Zum automatischen Berechnen der Anzahl von Verpackungseinheiten muss diese Einheit mit der Einheit in den Auftragspositionen übereinstimmen.</td>
</tr>
<tr class="odd">
<td>Zuteilung nach Tarifkategorien</td>
<td>Einrichten von Regeln, um zu definieren, wie Verpackungsmaterialbuchungen den Tarifkategorien zugewiesen werden sollen. Für jede Kombination einer Produktgruppe, eine Verpackungsklasse und ein Verpackungscode, können Sie ein oder mehrere Tarifkategorien einrichten, die Angebote enthalten (in Prozent ). Die Summe von Angeboten für jede Kombination muss 100 Prozent betragen.</td>
</tr>
</tbody>
</table>

## <a name="manually-create-packing-material-transactions"></a>Manuelles Erstellen von Verpackungsmaterialbuchungen
Gehen Sie folgendermaßen vor, um für Verpackungsmaterialbuchungen einen fakturierten Auftrag oder eine Bestellung zu erstellen:

1.  Auf der Seite **Verpackungsmaterialbuchungen** klicken Sie auf **Neu** und geben Sie die folgenden Informationen auf der Seite **Verpackungsmaterialbuchung erstellen** ein:
    -   Wählen Sie in der Liste eine Rechnungszeile aus.
    -   Wählen Sie einen Verpackungsmaterialcode aus der **Verpackungsmaterialcode**-Dropdownliste aus.
    -   Wählen Sie eine Verpackungsklasse aus der **Verpackungsklasse**-Dropdownliste aus.

2.  Klicken Sie auf **OK**.
3.  Aktivieren Sie das Kontrollkästchen **Gebühr berechnen**, um die Verpackungsmaterialgebührenkomponente der Auftragsposition für Berichte zu berechnen.
4.  Optional: Aktualisieren Sie die Felder **Verpackungseinheit**, **Verpackungseinheitenmenge** und **Verpackungseinheitsgewicht**.
5.  Klicken Sie auf **Speichern**.

## <a name="create-packing-material-transactions-from-sales-orders-and-purchase-orders"></a>Dient zum Erstellen und Ändern von Verpackungsmaterialbuchungen für Bestellpositionen.
Gewicht und Gebühren des Verpackungsmaterials werden sowohl für Bestell- als auch für Auftragspositionen ermittelt. In den Positionsdetails für jede Position können Sie die Verpackungseinheit und die Menge der Verpackungseinheit angeben. Wenn die Auftragsposition fakturiert wird, werden Verpackungsmaterialbuchungen erstellt, und das jeweilige Verpackungsmaterialgewicht wird ermittelt. Verpackungsmaterialgebühren werden beim Buchen der Rechnung weder berechnet noch fakturiert. **Hinweis:** Wenn dem Artikel in der ausgewählten Auftragsposition eine Verpackungseinheit zugeordnet wurde, werden die Verpackungseinheit und die Verpackungsmenge automatisch geladen. In diesem Fall wird die Menge basierend auf der bestellten Menge (in Lagereinheiten) geteilt durch den Faktor für die Verpackungseinheit berechnet. Beim Buchen der Auftragsposition werden die Verpackungseinheit und die Anzahl der Verpackungseinheiten aus der Auftragsposition verwendet. Die Werte können jedoch auf der Seite **Rechnung buchen** auf der Registerkarte **Positionsdetails** ändern. Es ist wichtig, wenn der Auftrag teilweise fakturiert wird.

## <a name="calculate-packing-material-fees"></a>Verpackungsmaterialgebühren berechnen
Verwenden Sie die Verpackungsmaterialberechnungserfassung, um Gebühren für das Verpackungsmaterial zu berechnen und den **Verpackungsmaterialgebühren** Bericht zu drucken.

1.  Klicken Sie auf **Neu** und geben Sie die folgenden Feldinformationen ein:
    -   **Datum ab**– Geben Sie das Startdatum des Journals an.
    -   **Datum bis**– Geben Sie das Enddatum des Journals an.
    -   **Speicherdetails** – Aktivieren Sie dieses Kontrollkästchen, wenn Sie Berechnungsdetails prüfen möchten.

2.  Klicken Sie auf **Positionen**. Die **Erfassungszeile**– erscheint und zeigen die zusammengefassten Daten an (gruppiert nach Tarifkategorie und Verpackungsmaterialcode).
3.  Klicken Sie auf **Berechnungsdetails**, um die **Berechnungsdetails**-Seite zu öffnen, in der alle Daten zu allen Buchungen für die Erfassungsperiode zu verschiedenen Tarifkategorien zugewiesen werden.

## <a name="print-the-packing-materials-fee-calculation-report"></a>Bericht "Berechnung der Verpackungsmaterialgebühren" drucken
Der Bericht **Berechnung der Verpackungsmaterialgebühren** enthält Daten zu Verpackungsmaterialgebühren, die berechnet wurden, indem österreichische Regeln eingerichtet werden. Um diesen Bericht zu drucken, wählen Sie auf der Seite **Verpackungsmaterialberechnungserfassung** die berechnete Erfassung aus und klicken dann **Bericht drucken**.



