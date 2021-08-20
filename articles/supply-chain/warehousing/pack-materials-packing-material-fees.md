---
title: Verpackungsmaterialien und Gebühren
description: Dieses Thema informiert über Verpackungsmaterialgebühren, die in bestimmten Abständen an Recyclingunternehmen gezahlt werden.
author: MarkusFogelberg
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d1ed614a036e1d2cbd16f4757ec7c69a1d02f1d2adc92b86203f184a0b5d106
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742535"
---
# <a name="packing-materials-and-fees"></a>Verpackungsmaterialien und Gebühren

[!include [banner](../includes/banner.md)]

Verpackungsmaterialgebühren werden in bestimmten Abständen an ein Recyclingunternehmen gezahlt. Für jedes Material, aus dem eine Verpackung besteht, muss ein bestimmter Betrag pro Gewichtseinheit bezahlt werden. Obwohl die Verpackungsmaterialgebühren berechnet und gemeldet werden, werden keine Buchhaltungsvorgänge gebucht, da die Gebühren nicht als Steuern betrachtet werden, die an eine Behörde gezahlt werden müssen.

Gewicht und Gebühren des Verpackungsmaterials werden sowohl für Bestell- als auch für Auftragspositionen ermittelt.

Sie können eine oder mehrere Verpackungseinheiten für einen einzelnen Artikel, eine Gruppe von Artikeln (Verpackungsgruppe) oder alle Artikel definieren. Eine Verpackungseinheit besteht neben der Anzahl der Artikel, die in der Verpackungseinheit enthalten sind, aus den verschiedenen Verpackungsmaterialien und ihrem jeweiligen Gewicht. Jedem definierten Typ von Verpackungsmaterial wird ein Verpackungsmaterialcode zugewiesen. Auf der Grundlage des Packmittelcodes können Sie einen Preis für einen bestimmten Zeitraum festlegen. Die Verpackungsmaterialgebühr wird anhand dieser Informationen berechnet.

> [!NOTE]
> Auch wenn Ihr Unternehmen keine Verpackungsmaterialgebühren zahlt, können Sie die Funktionalität zur Berechnung von Statistiken für die Gewichte von Verpackungsmaterialien nutzen.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Verpackungsmaterialzuordnung einrichten

Bevor Sie Verpackungsmaterialgewichte, Verpackungsmaterialgebühren oder beides berechnen können, müssen Sie die Berechnung einschalten und festlegen, welche Materialien und Gebühren für welche Positionen gelten.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Bestands- und Lagerverwaltungsparameter**.
1. Setzen Sie auf der Registerkarte **Allgemein** im Abschnitt **Verpackungsmaterial** die Option **Verpackungsmaterialgebühren berechnen** auf **Ja**.
1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Verpackungsmaterial \> Verpackungsgruppen**, und legen Sie alle von Ihnen verwendeten Verpackungsgruppen an. Alle Positionen in einer Verpackungsgruppe verwenden dieselbe Packmittelzuordnung. Wenn Sie keine Packmittelgruppen verwenden, können Sie diesen Schritt überspringen.

    > [!TIP]
    > Nachdem Sie Ihre Verpackungsgruppen angelegt haben, können Sie jedem Produkt eine Gruppe nach Ihren Wünschen zuordnen. Gehen Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**, wählen Sie ein Produkt aus und wählen Sie dann auf der Registerkarte **Bestandsverwaltung** im Feld **Verpackungsgruppe** die entsprechende Verpackungsgruppe.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Verpackungsmaterial \> Verpackungsmaterialcodes**, definieren Sie jede Art von Verpackungsmaterial, das Sie verwenden, und geben Sie die Einheit an, in der das Verpackungsmaterial bei der Vorbereitung von Sendungen verbraucht wird.
1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Verpackungsmaterial \> Verpackungsmaterialgebühren**, und legen Sie eine Gebühr für jede Art von Verpackungsmaterial fest, die Sie gerade definiert haben. Die Gebühren werden auf der Grundlage des Preises pro verbrauchter Einheit berechnet.
1. Um den Artikeln Verpackungsmaterial zuzuordnen, gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Verpackungsmaterial \> Verpackungsmaterialzuordnung**, und erstellen Sie Zuordnungen. Sie können so viele Zuordnungen anlegen, wie Sie benötigen. Sie können Packmittel für einzelne Positionen, Gruppen von Positionen (Verpackungsgruppen) oder alle Positionen zuordnen, je nachdem, wie detailliert Ihre Zuordnungen sein sollen.

    Führen Sie für jede Zuteilung, die Sie anlegen, die folgenden Schritte aus.

    1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

        - **Positionscode** - Wählen Sie den Umfang der Zuordnung aus:

            - **Tabelle** - Legen Sie eine Zuteilung für einen einzelnen spezifischen Artikel an.
            - **Gruppe** - Erstellen Sie eine Zuordnung für alle Artikel, die zu einer Verpackungsgruppe gehören, die auf der Seite **Verpackungsgruppen** definiert ist.
            - **Alles** - Erstellen Sie eine Zuordnung für alle Artikel.

            > [!NOTE]
            > Normalerweise sollten Sie alle Ihre Zuordnungen auf der gleichen Ebene vornehmen (**Tabelle**, **Gruppe** oder **Alle**). Wenn Sie mehr als eine Ebene verwenden, wird für jeden Artikel die spezifischste passende Zuordnung verwendet. (Die Ebene **Tabelle** hat Vorrang vor der Ebene **Gruppe**, und beide Ebenen haben Vorrang vor der Ebene **Alle**).

        - **Artikelrelation** - Wenn Sie einen einzelnen Artikel zuordnen, wählen Sie den Artikel aus. Wenn Sie für eine Gruppe von Artikeln aufteilen, wählen Sie die Verpackungsgruppe aus. Wenn Sie für alle Artikel aufteilen möchten, lassen Sie dieses Feld leer.
        - **Konfiguration**, **Größe**, **Farbe**, und **Stil** - Geben Sie die gewünschten Werte für diese Dimensionen ein, um die Position, die Sie zuordnen möchten, weiter zu definieren.
        - **Verpackungseinheit** - Wählen Sie die Einheit aus, in der der Artikel verpackt wird, wenn das Verpackungsmaterial verwendet wird. Diese Maßeinheit kann sich von der Einheit unterscheiden, in der der Artikel gekauft und gelagert wird.
        - **Packungseinheitsfaktor** - Geben Sie den Umrechnungsfaktor ein, der zur Umrechnung von der Bestands- in die Verpackungseinheit verwendet wird. (Die Umrechnung erfolgt nach der Formel *Verpackungseinheiten* = *Artikeleinheiten* × *Verpackungseinheiten-Faktor*).

    1. Fügen Sie auf der Registerkarte **Verpackungsmaterial** für jedes Stück Verpackungsmaterial, das für die aktuelle Zuordnung benötigt wird, eine Zeile hinzu. Geben Sie in jeder Zeile die Art des Materials (wie auf der Seite **Verpackungsmaterialcodes** definiert) und die Menge des Materials an, die für jede versandte Einheit des aktuellen Artikels verbraucht wird.

## <a name="packing-units-on-sales-order-lines"></a>Verpackungseinheiten in Auftragspositionen

Nachdem Sie [Berechnung der Verpackungsmaterialgebühren eingeschaltet und Ihre Zuordnungen](#allocations) eingerichtet haben, prüft das System, ob für jede Position, die einem Kundenauftrag hinzugefügt wird, Verpackungseinheiten angegeben sind. Anschließend berechnet es die erforderlichen Gebühren. Wenn ein Artikel zu einem Kundenauftrag hinzugefügt wird, erfolgt einer der folgenden Schritte:

- **Wenn für den Artikel eine Verpackungszuordnung gilt:** Das System aktualisiert die Kundenauftragszeile mit der angegebenen Verpackungseinheit und der Verpackungseinheitsmenge. (Die Verpackungseinheitsmenge wird nach der Formel *Verpackungseinheitsmenge* = *Bestellte Menge* ÷ *Anzahl der Positionen in der ausgewählten Verpackungseinheit* berechnet).
- **Wenn keine Verpackungszuordnung für die Position gilt:** Sie können in der Kundenauftragszeile eine Verpackungseinheit und eine Verpackungseinheitsmenge manuell eingeben.

Es ist auch möglich, die Verpackungseinheit und die Verpackungseinheitenmenge beim Buchen der Auftragsposition zu ändern. Diese Fähigkeit ist relevant, wenn die Kundenauftragszeile nur teilweise geliefert oder teilweise fakturiert wird.

Wenn Sie den Kundenauftrag fakturieren, legt das System Packmitteltransaktionen an. Verpackungsmaterialbuchungen enthalten die Gewichtungen des Verpackungsmaterials für die Auftragsposition. Sie können die Transaktionen nach der Fakturierung ändern. Anschließend können Sie neue Transaktionen anlegen.

## <a name="packing-units-on-purchase-order-lines"></a>Verpackungseinheiten in Bestellpositionen

Das System legt keine Packmitteltransaktionen für Bestellpositionen an. Stattdessen legen Sie manuell Transaktionen für fakturierte Bestellzeilen auf der Seite **Packmitteltransaktionen** an.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Einrichten von Lizenznummern für Kunden, denen Verpackungsmaterialgebühren berechnet werden

Wenn die Kundenaufträge für einen bestimmten Kunden Gebühren für die Verpackungsmaterialien enthalten sollen, die für jeden Auftrag verwendet werden, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Wählen Sie den Debitor aus, der für die Verpackungsmaterialien berechnet werden soll.
1. Setzen Sie auf der Registerkarte **Rechnung und Lieferung** die folgenden Felder:

    - Im Abschnitt **Umsatzsteuer** geben Sie im Feld **Verpackungssteuer-Lizenznummer** die Lizenznummer des Unternehmens ein.
    - Geben Sie im Abschnitt **Verpackungsmaterialgebühr** im Feld **Lizenznummer** die Lizenznummer der Firma ein.

Wenn Sie nun einen Kundenauftrag anlegen und fakturieren, der eine oder mehrere Positionen enthält, die Verpackungsmaterial verwenden, werden die Verpackungsmaterialgebühren in der Rechnung ausgewiesen.

Für Debitoren, die keine Verpackungsmaterialgebühren zahlen sollen, führen Sie die gleichen Schritte aus, aber löschen Sie die Lizenznummern aus den Feldern **Packgebühr-Lizenznummer** und **Lizenznummer**. Rechnungen für Debitoren, die keine Verpackungsmaterialgebühren zahlen, weisen zwar das Gewicht der Verpackungsmaterialien, aber nicht die Gebühren aus.

Um einen Bericht zu erstellen, der alle Verpackungsmaterialgebühren anzeigt, die Ihr Unternehmen für einen bestimmten Zeitraum schuldet, gehen Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Verpackungsmaterialberichte \> Verpackungsmaterialgebührenberechnung**, geben Sie einen Datumsbereich an und wählen Sie dann **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Angeben des Verpackungsmaterialgewichts auf Rechnungen

Sie können das Gewicht des Verpackungsmaterials auf einer Rechnung ausdrucken und angeben, wer die entsprechenden Gebühren bezahlt. Das Gewicht wird nach Verpackungscode zusammengefasst.

1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
1. Auf der Registerkarte **Aktualisierungen**, auf der Registerkarte **Rechnung** FastTab, setzen Sie die Option **Verpackungsmaterialgewicht drucken** auf **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]