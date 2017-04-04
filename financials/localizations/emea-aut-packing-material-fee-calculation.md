---
title: "Berechnung der Verpackungsmaterialgebühren für Österreich"
description: "Dieses Thema enthält Informationen zu Verpackungsmaterialsätze und Gebühren in Österreich."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 268034
ms.assetid: e53cec3e-0f87-4c1c-9685-74adbf5592ef
ms.search.region: Austria
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 39874b32184221d165ca7ed3b89cf7524c43f28c
ms.lasthandoff: 03/31/2017


---

# <a name="packing-material-fee-calculation-for-austria"></a>Berechnung der Verpackungsmaterialgebühren für Österreich

Dieses Thema enthält Informationen zu Verpackungsmaterialsätze und Gebühren in Österreich.

In Europa gibt es Verpackungsmüll Bestimmungen zu. Diese Bestimmungen arbeiten mit dem Prinzip "Kollektivproducerzuständigkeit. " Das bedeutet, er die Anforderung erzwingen, die der Verkäufer oder Hersteller Verpackung Umwelteinwirkung dieser Zuständigkeit für die Verpackung in Anspruch nehmen. Entsprechend den Bestimmungen Hersteller werden müssen, einen Teil der Kosten und des Wiederverwendens der Beitreibung der Verpackung zu bezahlen. Diese Zahlung bekannt als Verpackungsmaterial, und es fee* * hat ein Recyclingunternehmen regelmäßig bezahlt. Ein Unternehmen muss das Gewicht jeder Typ Verpackungsmaterial Papier (, Plastik, Metall, usw.) berechnen das während eines Verkaufs oder eines Einkaufs verwendet wurde, und dass Gewicht nach den im Satz des Pakets multiplizieren. Die Regierungsbehörde stellt den im Satz des Pakets für jeden Typ Verpackungsmaterial bereit. In Österreich ist eine Formel für komplexere für Verpackungsmaterialgebühren verwendet. Verpackungsmaterialien werden in verschiedene Kategorien gruppieren (beispielsweise, Haushalt und Werbung" dividiert, und stellt für die Behörde von Verpackungsmaterialien in den einzelnen Kategorien verfügbar. Die Kategorie, dass Verpackungsmaterial gehört, hängt von der Größe und die Produkte aus, die für die Verpackung verwendet wurde. Verpackungsmaterialgebühren werden kalkuliert und erfasst, es werden jedoch keine Sachkontobuchungen automatisch ausgeführt, da die Gebühren nicht als Steuern betrachtet werden, die an eine Behörde zu entrichten sind.

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
<td>Kategoriehierarchien Sie müssen für Produkte erstellen. Für jede müssen Sie Knoten Kategoriehierarchie erstellen, die als Produktgruppen für die Berechnung der Verpackungsmaterialgebühren verwendet werden. Sie müssen einen Kategoriehierarchietyp für Verpackungsmaterialien erstellen und die Kategoriehierarchie auf setzen. <strong>Verpackung</strong> <strong></strong><strong>Hinweis:</strong> Sie können eine Verpackungskategoriehierarchie für nur ein Kategoriehierarchietyp einrichten. Nachdem Sie Kategoriehierarchien erstellen, führen Sie die folgenden Schritte aus, um ein Produkt in einer Kategoriehierarchie zuzuordnen.
<ol>
<li>Wählen Sie auf der <strong>Produkte</strong> Seite in der Liste ein Produkt aus.</li>
<li>Klicken <strong>Produkt</strong>  <strong>Produktkategorien</strong> Sie auf der Registerkarte auf.</li>
</ol></td>
</tr>
<tr class="even">
<td>Verpackungsklassen</td>
<td>Erstellen oder Verwalten von Verpackungsklassen für die Berechnung der Verpackungsmaterialgebühren bei.</td>
</tr>
<tr class="odd">
<td>Zeichnen Sie Kategorien aus</td>
<td>Erstellen oder Verwalten von Tarifkategorien für die Berechnung der Verpackungsmaterialgebühren bei.</td>
</tr>
<tr class="even">
<td>Verpackungsmaterialcode</td>
<td>Erstellen Sie Verpackungsmaterialcodes für jeden Typ, das Verpackungsmaterial festgelegten Ebene.</td>
</tr>
<tr class="odd">
<td>Verpackungsmaterialgebühr</td>
<td>Geben Sie Verpackungsmaterialgebühren für jeden Verpackungsmaterialcode an. Jeden Materialtyp, definieren Sie den Gültigkeitszeitraum, Tarifkategorie, den Preis pro Material, die Währung und die Einheit.</td>
</tr>
<tr class="even">
<td>Verpackungsmaterialzuteilung</td>
<td>Legen Sie fest, welche Materialien in einer Verpackungseinheit enthalten sind, um Gewichte Sie zuweisen und die Gesamtanzahl von Artikeln angezeigt, die in der Verpackungseinheit enthalten sind. Sie können Verpackungseinheiten für einzelne Artikel, Verpackungsgruppen für oder für alle Artikel festlegen. <strong>Hinweis:</strong> Wenn Sie die Verpackungseinheit aus, Sie können die Verpackungseinheit laden und die Anzahl von Verpackungseinheiten ein, die automatisch auf lassen. Allerdings kann die Berechnung automatisch ausgeführt werden, wenn die Verpackungseinheit dieselbe, ist die Einheit in den Auftragspositionen übereinstimmen.</td>
</tr>
<tr class="odd">
<td>Zuweisung von Tarifkategorien</td>
<td>Einrichten von Regeln, um zu definieren, z Verpackungsmaterialbuchungen zu den Tarifkategorien zugewiesen werden sollen. Für jede Kombination einer Produktgruppe, eine und ein Verpackungsklasse Verpackungscode, können Sie ein oder mehrere Tarifkategorien einrichten, Angebote enthalten (in Prozent ). Die Summe von Angeboten für jede Kombination muss 100 Prozent betragen.</td>
</tr>
</tbody>
</table>

## <a name="manually-create-packing-material-transactions"></a>Manuelles Erstellen von Verpackungsmaterialbuchungen
Gehen Sie folgendermaßen vor, um für Verpackungsmaterialbuchungen einen fakturierten Auftrag oder eine Bestellung zu erstellen:

1.  ** Verpackungsmaterialbuchungen ** Auf der Seite klicken ** ** Sie neu, und geben Sie die folgenden Informationen zur jeweiligen ** Erstellen Verpackungsmaterialbuchung ** Seite ein:
    -   Wählen Sie eine Rechnungsposition in der Liste aus.
    -   Wählen Sie einen aus der Verpackungsmaterialcode ** Verpackungsmaterialcode ** Dropdownliste aus.
    -   Wählen Sie eine Verpackungsklasse von der Verpackungsklasse ** ** Dropdownliste aus.

2.  Click **OK**.
3.  Wählen Sie das ** berechnen Sie Gebühr ** Kontrollkästchen, um die Verpackungsmaterialgebührenkomponente der Auftragsposition für die Berichterstellung zu berechnen.
4.  Optional: Aktualisieren Sie ** Verpackungseinheit **, ** Verpackungseinheitenmenge ** und Verpackungseinheitsgewicht ** ** Felder.
5.  Click **Save**.

## <a name="create-packing-material-transactions-from-sales-orders-and-purchase-orders"></a>Erstellen von Verpackungsmaterialbuchungen von Aufträgen und Bestellungen
Gewicht und Gebühren des Verpackungsmaterials werden für Auftragspositionen und Bestellpositionen berechnet. Ausführlich die Positionsdetails für jede Position, können Sie der Verpackungseinheit und der Menge der Verpackungseinheit angeben. Wenn eine Auftragsposition fakturiert wird, werden Verpackungsmaterialbuchungen erstellt, und das Gewicht des Verpackungsmaterials berechnet werden. Verpackungsmaterialgebühren werden nicht berechnet, wenn die Rechnung gebucht wird, und sie werden nicht fakturiert. ** Hinweis: ** Wenn eine Verpackungseinheit dem Artikel in der ausgewählten Auftragsposition zugeordnet wurde, werden die Verpackungseinheit und die Verpackungseinheits Avismenge automatisch geladen. In diesem Fall wird die Menge berechnet, z die bestellte Menge (in Lagereinheiten) durch den Verpackungseinheitsfaktor des Besitzers dividiert wird. Beim Buchen wird, werden die Verpackungseinheit und die Verpackungseinheits Avismenge aus der Auftragsposition verwendet. Die Werte können jedoch auf der Seite Buchungsrechnung ** ** ** Positionsdetails ** auf der Registerkarte ändern. Es ist wichtig, wenn der Auftrag teilweise fakturiert wird.

## <a name="calculate-packing-material-fees"></a>Verpackungsmaterialgebühren berechnen
Verwenden Sie die Verpackungsmaterialberechnungserfassung, um Gebühren für das Verpackungsmaterial zu berechnen und den ** Verpackungsmaterialgebühren ** Bericht zu drucken.

1.  ** Der auf neu ** und geben die folgenden Informationen ein:
    -   ** Ab Sie ** – angeben dem Startdatum der Erfassung.
    -   ** Datum zu ** – Gibt das Enddatum der Erfassung an.
    -   ** Abwehrdetails ** - Aktivieren Sie dieses Kontrollkästchen, wenn Sie Berechnungsdetails prüfen möchten.

2.  Klicken Sie auf **Positionen**. ** Die Erfassungspositionen ** Seite erscheint und werden die zusammengefasste Daten angezeigt (gruppiert nach Tarifkategorie Verpackungsmaterialcode und).
3.  ** Auf Berechnungsdetails ** um die Berechnungsdetails ** ** Seite zu öffnen, in der alle Daten zu allen Buchungen für die Erfassungsperiode zu verschiedenen Tarifkategorien zugewiesen werden.

## <a name="print-the-packing-materials-fee-calculation-report"></a>Drucken des Berichts zur Berechnung der Verpackungsmaterialgebühr
** Berechnung der Verpackungsmaterialgebühren ** Der Bericht enthält Daten zu Verpackungsmaterialgebühren, die berechnet wurden, indem österreichische Regeln eingerichtet werden. Um diesen Bericht darüber, welche Verpackungsmaterialberechnungserfassung ** ** Seite drucken möchten, aktivieren die berechnete Erfassung aus und klicken dann Drucktbericht ** **.


