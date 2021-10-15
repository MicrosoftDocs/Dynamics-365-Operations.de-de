---
title: Gefährliche Stoffe in Produkten, Bestellungen, Sendungen und Ladungen
description: In diesem Thema wird erläutert, wie Sie die gefährliche Stoffe für freigegebene Produkte festlegen, wie Sie Bestandsbeschränkungen für Gefahrengüter festlegen und wie Sie gefährliche Stoffe in einen Auftrag, eine Lieferung oder eine Ladung einbeziehen.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 64d31cd86045ff28aa007666a3877271eecf0106
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570704"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Gefährliche Stoffe in Produkten, Bestellungen, Sendungen und Ladungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die gefährliche Stoffe für freigegebene Produkte festlegen, wie Sie Bestandsbeschränkungen für Gefahrengüter festlegen und wie Sie gefährliche Stoffe in einen Auftrag, eine Lieferung oder eine Ladung einbeziehen.

## <a name="set-hazardous-material-specifications-for-products"></a>Angaben zu gefährlichen Stoffen für Produkte festlegen

Nachdem Sie eine Gefahrstoffverordnung definiert und die zugehörigen Referenzcodes wie in [Gefahrstoffe einrichten](hazmat-setup.md) beschrieben eingerichtet haben, können Sie diese Informationen mit freigegebenen Artikeln verknüpfen. Der Versandtext für Versanddokumente wird aus den Gefahrstoffinformationen für die freigegebenen Artikel entnommen.

Im Rahmen der Zuordnung eines freigegebenen Artikels zu einem gefährlichen Material müssen Sie den Vorschriftscode und das Material angeben. Abhängig von den Transportarten können einem Artikel unterschiedliche Vorschriftencodes zugeordnet sein, und Sie können jedem Artikel mehrere Vorschriften- und Materialcodes zuordnen.

Befolgen Sie diese Schritte, um ein freigegebenes Produkt als Gefahrgut einzurichten.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie ein Produkt aus oder erstellen Sie es, um seine Seite **Freigegebene Produktdetails** zu öffnen.
1. Auf dem Inforegister **Lagerbestand verwalten** legen Sie die Option **Gefährlicher Stoff** auf **Ja** fest. Diese Einstellung identifiziert den Artikel als gefährliches Gut und wird verwendet, wenn Versanddokumente gedruckt werden.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Konformität** die Option **Gefahrstoff des Artikels** aus.
1. Füllen Sie die Seite **Gefahrstoffe des Artikels** für den ausgewählten Artikel aus, indem sie die Felder verwenden, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="item-hazardous-materials-header"></a>Gefahrstoffe des Artikels – Kopfzeile

In der folgenden Tabelle werden die Felder beschrieben, die oben auf der Seite **Gefahrstoffe des Artikels** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Artikelnummer | Das veröffentlichte Produkt, mit dem Sie arbeiten. |
| Bestimmungscode | Wählen Sie die für das Produkt geltende Gefahrstoffverordnung aus. Die Verordnung legt fest, wie der gedruckte Versandtext für einen Artikel und die damit verbundenen Lieferarten erstellt wird. Nach der Zuweisung kann der Code auf dieser Seite nicht mehr bearbeitet werden. Sie können jedoch durch Auswahl einen neuen Vorschriftscode zuweisen, indem Sie **Neu** auswählen. |
| Materialcode | (Optional) Wählen Sie den für das Produkt geltenden Gefahrstoffcode aus. Der Materialcode enthält eine Vorlage, die Standardwerte für viele andere Felder auf dieser Seite enthält. Wenn Sie einen Code auswählen, werden alle Gefahrstoffangaben in das aktuelle Produkt kopiert. Das System fordert Sie jedoch zunächst auf, zu bestätigen, dass Artikelmaterialdaten aus dem Materialcode eingegeben werden sollen. |
| Gruppencode | (Optional) Wählen Sie die für das Produkt geltende Gefahrstoffklassifizierungsgruppe aus. Bezüglich des Felds **Materialcode**, wenn Sie einen Code auswählen, werden alle Gefahrstoffangaben in das aktuelle Produkt kopiert. Das System fordert Sie jedoch zunächst auf, zu bestätigen, dass Artikelklassengruppen-Daten aus dem Gruppencode eingegeben werden sollen. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Beschreibungen-Inforegister

In der folgenden Tabelle werden die Felder beschrieben, die im Inforegister **Beschreibungen** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Ordnungsgemäßer Versandname | Geben Sie die Standardbeschreibung für das Material ein, wie in der geltenden Verordnung angegeben. Sie können Übersetzungen für diesen Wert im Inforegister **Artikelversandtext-Übersetzung** bereitstellen, wie im nächsten Abschnitt beschrieben. |
| Technischer Name | Wählen Sie den allgemeinen oder generischen Namen für das Material. Dieser Name kann ein Name sein, den Ihr Unternehmen intern für das Material verwendet. |
| N.O.S. | Aktivieren Sie dieses Kontrollkästchen, um anzuzeigen, dass der Wert **Korrekter Versandname** ein nicht anderweitig spezifischer (N.O.S.) Versandname für den Artikel ist. N.O.S. Versandnamen werden für Gruppen ähnlicher Chemikalien und Materialien verwendet, die bestimmte Endanwendungen haben, die jedoch in einer bestimmten Verordnung möglicherweise nicht namentlich in der Gefahrstofftabelle aufgeführt sind. |

### <a name="item-ship-text-translation-fasttab"></a>Artikelversandtext-Übersetzung – Inforegister

Das Inforegister **Artikelversandtext-Übersetzung** enthält ein Raster, das Übersetzungen der Werte **Korrekter Versandname** anzeigt, die für die Primärsprache im Inforegister **Beschreibungen** definiert sind. Diese Übersetzungen können beim Versanddrucktext für mindestens eine weitere Sprache verwendet werden.

In der folgenden Tabelle werden die Felder beschrieben, die im Inforegister **Artikelversandtext-Übersetzung** verfügbar sind.


| Feld | Beschreibung |
|---|---|
| Sprache | Der Sprachcode, den die Zeile verwendet. Beispielsweise **pt-br** zeigt brasilianisches Portugiesisch an. |
| Versanddrucktext | Der übersetzte Wert **Korrekter Versandname** in der Sprache, die die Zeile verwendet. |

Wählen Sie zum Hinzufügen oder Bearbeiten einer Übersetzung **Übersetzungen** über dem Gitter aus, um die Seite **Textübersetzungen** zu öffnen. Folgen Sie dann diesen Schritten:

- Um eine neue Übersetzung hinzuzufügen, wählen Sie im Aktionsbereich **Hinzufügen** aus. Wählen Sie die Sprache aus, die Sie hinzufügen möchten, und geben Sie dann im Feld **Übersetzter Text** den übersetzten Text ein.
- Um eine vorhandene Übersetzung zu bearbeiten, wählen Sie eine Zielsprache im Feld **Sprache** aus, und bearbeiten Sie den übersetzten Text im Feld **Übersetzter Text** nach Bedarf.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Materialverwaltung – Inforegister

In der folgenden Tabelle werden die Felder beschrieben, die im Inforegister **Materialverwaltung** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Klasse  | Wählen Sie die Gefahrstoffklasse aus, zu der das Produkt gehört, wie in der Verordnung definiert, der Sie entsprechen. Sie müssen jedem Produkt, das gefährliche Materialien enthält, sowohl eine Sparte als auch eine Klasse zuweisen. |
| Beschreibung | Die Beschreibung, die für die ausgewählte Klasse definiert ist, wird im Feld **Klasse** ausgewählt. Dieses Feld ist schreibgeschützt. |
| Division | Wählen Sie die Gefahrstoffsparte aus, zu der das Produkt gehört, wie in der Verordnung definiert, der Sie entsprechen. Die Sparte ist eine Teilmenge der Klasse. Sie müssen jedem Produkt, das gefährliche Materialien enthält, sowohl eine Sparte als auch eine Klasse zuweisen. |
| Kennung | Wählen Sie den Gefahrstoff-Kennungscode aus. In der Regel basiert dieser Code auf einem Standard der Vereinten Nationen (UN). |
| Verpackungsgruppe | Wählen Sie die Verpackungsgruppe aus, die für den aktuellen Artikel gilt. |
| Beschreibung | Die Beschreibung, die für die Gruppe definiert ist, die im Feld **Verpackungsgruppe** ausgewählt ist. Dieses Feld ist schreibgeschützt. |
| Verpackungsbeschreibungen | Wählen Sie den entsprechenden Verpackungsbeschreibungscode aus. Dieser Code verweist auf eine Beschreibung, die angibt, wie das Produkt verpackt werden muss. |
| Gefahrstoffetikette | Wählen Sie einen Code aus, der auf das zutreffende Gefahrgutetikett verweist, das auf das Produkt aufgebracht werden soll. |
| Begrenzte Menge | Legen Sie diese Option auf **Ja** fest, um das Gesamtproduktgewicht anzugeben, das in jeder Ladung und in jeder Ladeposition enthalten ist. |
| Leistung | Geben Sie die Menge des gefährlichen Materials im Produkt in der angegebenen Einheit ein. Dieser Wert wird verwendet, um die Gesamtbewertung gefährlicher Stoffe für Ladungen und Lieferungen zu berechnen, die das Produkt enthalten. |
| Multiplikator | Geben Sie den Multiplikator ein, der angewendet wird, wenn die Bewertung des Gefahrstoffs für jede Ladungsposition berechnet wird, die das Produkt enthält. Dieser Wert wird durch die gültige Vorschrift vorgegeben, gemäß dem Typ des Gefahrstoffs, der im Produkt enthalten ist. |
| Einheit | Wählen Sie die Maßeinheit aus, die für die Menge der Gefahrstoffe im Produkt gilt, wie im Feld **Menge** angegeben. Dieser Wert wird verwendet, um die Gesamtbewertung gefährlicher Stoffe für Ladungen und Lieferungen zu berechnen, die das Produkt enthalten. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>So wird der Gefahrstoffwert berechnet

Mehrere der Werte, die im Inforegister **Materialverwaltung** für ein Produkt angegeben werden, werden zur Berechnung einer *Gefahrstoffbewertung* für jede Ladungsposition verwendet, die das Produkt enthält. Der Wert wird mithilfe der folgenden Formel berechnet:

Gefahrstoffbewertung = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Hier ist ein Schlüssel für die Formel:

- *&lt;LineQty&gt;* ist die Menge des Produkts, das für eine Ladungsposition angegeben ist.
- *&lt;HazmatQty&gt;* ist die Menge des Gefahrstoffs, der für ein Produkt im Feld **Menge** im Inforegister **Materialverwaltung** angegeben ist.
- *&lt;Einheitsumrechnung&gt;* ist ein Umrechnungsfaktor zum Umrechnen zwischen der Einheit, die für die Ladungspositionsmenge verwendet wird und der Einheit, die für ein Produkt im Feld **Einheit** im Inforegister **Materialverwaltung** angegeben ist.
- *&lt;Multiplier&gt;* ist der Multiplikator, der für ein Produkt im Feld **Multiplikator** im Inforegister **Materialverwaltung** angegeben ist.

Diese Bewertung wird für jede Ladungsposition gemeldet, die ein Produkt enthält, für das diese Werte angegeben sind. Weitere Informationen finden Sie unter [Lieferungen, die Gefahrstoffe enthalten](#hazmat-shipments) und im Abschnitt [Ladungen, die Gefahrstoffe enthalten](#hazmat-loads) später in diesem Thema.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>So wird das Gefahrstoffgewicht berechnet

Ladungen und Ladungspositionen, die Produkte enthalten, bei denen die Option **Begrenzte Menge** im Inforegister **Materialverwaltung** auf **Ja** festgelegt ist, zeigen das Gefahrstoff-Gesamtgewicht an, wie beschrieben in den Abschnitten [Lieferungen, die Gefahrstoffe enthalten](#hazmat-shipments) und [Ladungen, die Gefahrstoffe enthalten](#hazmat-loads) später in diesem Thema. Das Gefahrstoffgewicht wird mithilfe der folgenden Formel berechnet:

Gefahrstoffgewicht = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Hier ist ein Schlüssel für die Formel:

- *&lt;LineQty&gt;* ist die Menge des Produkts, das für eine Ladungsposition angegeben ist.
- *&lt;ProductWeight&gt;* ist das Gewicht, das für das Produkt angegeben ist, in der Lagerbestandseinheit, die für das Produkt angegeben ist.
- *&lt;UnitConversion&gt;* ist ein Umrechnungsfaktor zum Umrechnen zwischen der Einheit, die für die Ladungspositionsmenge verwendet wird und der Lagerbestandseinheit, die für *&lt;ProductWeight&gt;* verwendet wird.

### <a name="transport-information-fasttab"></a>Transportinformationen – Inforegister

Die folgende Tabelle beschreibt die Felder, die im Inforegister **Transportinformationen** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Transportkategorie | Wählen Sie die zugehörige Transportkategorie. |
| Tunnelcode | Wählen Sie den zugehörigen Tunneleinschränkungscode für den Artikel aus. |
| Gefahrengüterverladung | Wählen Sie den Referenzcode aus, der für die Verstauung von Seefracht verwendet wird, wenn der Artikel per Seefracht geliefert wird. |
| Flugzeugtyp | Wählen Sie die Flugzeugbeschränkung aus, die für das Material gilt, wenn es per Luftfracht geliefert wird. |
| Verpackung – nur Frachtflugzeuge | Basierend auf dem Wert, den Sie im Feld **Flugzeugtyp** ausgewählt haben, wählen Sie den Verpackungsanweisungscode aus, der gilt, wenn das Produkt nur mit Frachtflugzeugen versendet werden kann. |
| Verpackung – Passagier- und Frachtflugzeug | Basierend auf dem Wert, den Sie im Feld **Flugzeugtyp** ausgewählt haben, wählen Sie den Verpackungsanweisungscode aus, der gilt, wenn das Produkt entweder mit Frachtflugzeugen oder mit Passagierflugzeugen versendet werden kann. |
| IATA-Stern | Legen Sie diese Option auf **Ja** fest, um anzuzeigen, dass die Lufttransportspezifikationen, die in diesem Inforegister eingegeben werden, mit dem Gefahrgutstandard der International Air Transport Association (IATA) übereinstimmen. Dieses Feld dient nur zu Informationszwecken. |
| Notfallreaktion | Wählen Sie den Code aus, der auf Anweisungen zum Umgang mit dem Material im Notfall verweist. |

### <a name="environmental-information-fasttab"></a>Umweltinformationen – Inforegister

Die folgende Tabelle beschreibt die Felder, die im Inforegister **Umweltinformationen** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Gefährlich für die Umwelt | Legen Sie diese Option auf **Ja** fest, um anzuzeigen, dass das Produkt umweltgefährdend ist. Verwenden Sie dieses Feld für Ihre eigenen Berichtszwecke. |
| Meeresschadstoff | Legen Sie diese Option auf **Ja** fest, um anzuzeigen, dass das Produkt ein Schadstoff für das Meer ist. Verwenden Sie dieses Feld für Ihre eigenen Berichtszwecke. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Bestandsgrenzen für gefährliche Produkte festlegen

Aus Sicherheitsgründen müssen Sie möglicherweise die Gesamtmenge eines bestimmten Produkts begrenzen, das an einem einzigen Standort gelagert werden kann. Um Bestandsgrenzen für ein zugelassenes Produkt festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie ein Produkt aus, um seine Seite **Details zum zugelassenen Produkt** zu öffnen.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Konformität** die Option **Berichterstellungsdetails** aus.
1. In den Feldern **Gefahrstoffbegrenzung** und **Grenzwert für Gefahrenwarnungen** legen Sie die entsprechenden Werte für das ausgewählte Produkt fest.

Anhand des Berichts **Lagerbestandsgrenze für gefährliche Stoffe** können Sie Lagerbestandsmengen der Gefahrstoffe an Ihren Lagerorten überwachen, um sicherzustellen, dass diese unter den hier festgelegten Sicherheitsgrenzen bleiben. Weitere Informationen finden Sie unter [Bericht über Grenzwerte für gefährliche Stoffe](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Auftragstransaktionen, die Gefahrstoffe umfassen

Um ein Produkt, das als Gefahrgut eingestuft ist, in einen Auftrag aufzunehmen, müssen Sie dem Auftrag den entsprechenden Spediteur zuordnen. Öffnen Sie den Auftrag, und legen Sie dann im Inforegister **Lieferung** den **Spediteur** und **Spediteurdienst** wie erforderlich fest.

Der Spediteurs ist auch der Lieferart zugeordnet. Daher müssen Sie sicherstellen, dass diese Informationen mit der Gefahrstoffverordnung übereinstimmen. Mit anderen Worten, die in der Gefahrstoffverordnung festgelegte Lieferart muss mit den Angaben in der Kopfzeile des Auftrags übereinstimmen. Auf diese Weise werden die Verordnung, der Spediteur und der Dienst mit den Lieferpositionen verbunden, die in einem Auftrag verwendet werden.

Nachdem ein Kundenauftrag abgeschlossen und versandbereit ist, kann er an das Lager freigegeben werden, um den Übergang von Verkauf zu Lagervorgängen anzuzeigen.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Lieferungen mit Gefahrstoffen

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Gefahrstoffwerte für jede Lieferposition anzeigen

Die Seite **Lieferungsdetails** für eine Lieferung zeigt das Gefahrstoff-Gesamtgewicht und Punktwerte an, die für jede Ladungsposition berechnet wurden, die in dieser Lieferung enthalten sind. Führen Sie diese Schritte aus, um die Bewertungen und Gewichte anzuzeigen.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Wählen Sie ein Lieferung aus, um ihre Seite **Lieferungsdetails** zu öffnen.
1. Im Inforegister **Ladungspositionen** überprüfen Sie die Positionen. Für jede Position sehen Sie die Gefahrstoffberechnungen in den folgenden Feldern:

    - **Gefahrstoffpunkte** – Dieses Feld zeigt die Gefahrstoffbewertung für die Ladungsposition. Der Wert wird gemäß den Regeln und Werten berechnet, die für die geltende Verordnung und in der Einrichtung des zugelassenen Produkts ermittelt wurden. Die Berechnung nimmt die Menge auf der Ladungsposition und verweist auf den Multiplikator in der [Materialverwaltungs-Setup](#material-management) für das zugelassene Produkt.
    - **Begrenzte Menge – Nettogewicht** – Für Produkte, die aufgrund ihres Gefahrstoffgehalts als Produkte mit begrenzter Menge gekennzeichnet sind, zeigt dieses Feld das Gesamtnettogewicht des Gefahrstoffgehalts an, das in der Ladungsposition enthalten ist. Die Berechnung basiert auf den Produkten, die im Setup des zugelassenen Produkts als Gefahrstoffe gekennzeichnet sind. Wenn ein Artikel als Artikel mit begrenzter Menge markiert ist, nimmt die Berechnung die Menge zu jeder Ladungsposition und verweist auf das Gewicht im [Materialverwaltungs-Setup](#material-management) für das zugelassene Produkt.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Überprüfen Sie die Kompatibilität verschiedener gefährlicher Materialien, die in einer Lieferung enthalten sind

Das System kann bewerten, ob alle in einer Lieferung enthaltenen gefährlichen Materialien für den gemeinsamen Versand geeignet sind. Um die Kompatibilität zu bewerten, überprüft das System die Kompatibilitätsgruppe, die jedem Produkt zugewiesen ist, das in der Lieferung enthalten ist. Weitere Informationen finden Sie unter [Kompatibilitätsgruppen für Gefahrstoffe](hazmat-setup.md#compatibility-groups).

Gehen Sie folgendermaßen vor, um die Kompatibilitätsprüfung auszuführen.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Wählen Sie ein Lieferung aus, um ihre Seite **Lieferungsdetails** zu öffnen.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Lieferungen** in der Gruppe **Aktionen** die Option **Kompatibilitätsprüfung** aus.

Sie erhalten eine Nachricht, die Sie über die Ergebnisse der Prüfung informiert.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Ladungen mit Gefahrstoffen

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Gefahrstoffbewertungen für jede Ladungsposition anzeigen

Die Seite **Ladungsdetails** für eine Ladung zeigt das Gefahrstoff-Gesamtgewicht und Punktwerte an, die für diese Ladung und jede Ladungsposition berechnet wurden. Führen Sie diese Schritte aus, um die Bewertungen und Gewichte anzuzeigen.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Ladungen**.
1. Wählen Sie ein Ladung aus, um ihre Seite **Ladungsdetails** zu öffnen. (Sie können Ladungsdetails auch öffnen, indem Sie einen Link aus einer zugehörigen Lieferung auswählen.)
1. Im Inforegister **Ladung** können Sie die Gefahrstoff-Gesamtbewertungen und -Gewichte für die gesamte Ladung überprüfen, indem Sie die folgenden Felder überprüfen:

    - **Gefahrstoffpunkte** – Dieses Feld zeigt die Gefahrstoffbewertung für die Ladung an. Der Wert wird gemäß den Regeln und Werten berechnet, die für die geltende Verordnung und in der Einrichtung des zugelassenen Produkts ermittelt wurden. Die Berechnung nimmt die Menge, die in der Ladung enthalten ist, und verweist auf den Multiplikator im [Materialverwaltungs-Setup](#material-management) für das zugelassene Produkt.
    - **Begrenzte Menge – Nettogewicht** – Für Produkte, die aufgrund ihres Gefahrstoffgehalts als Produkte mit begrenzter Menge gekennzeichnet sind, zeigt dieses Feld das Gesamtnettogewicht des Gefahrstoffgehalts an, das in der Ladung enthalten ist. Die Berechnung basiert auf den Produkten, die im Setup des zugelassenen Produkts als Gefahrstoffe gekennzeichnet sind. Wenn ein Artikel als Artikel mit begrenzter Menge markiert ist, nimmt die Berechnung die Menge in jeder Ladung und verweist auf das Gewicht im [Materialverwaltungs-Setup](#material-management) für das zugelassene Produkt.

1. Um die Bewertungen und Gewichte für einzelne Positionen zu überprüfen, wählen Sie das Inforegister **Ladungen laden** aus. Die Werte, die für jede Position angegeben werden, ähneln den Werten, die für die gesamte Ladung bereitgestellt werden, wie im vorherigen Schritt beschrieben.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Überprüfen Sie die Kompatibilität verschiedener gefährlicher Materialien, die in einer Ladung enthalten sind

Das System kann bewerten, ob alle in einer Ladung enthaltenen gefährlichen Materialien für den gemeinsamen Versand geeignet sind. Um die Kompatibilität zu bewerten, überprüft das System die Kompatibilitätsgruppe, die jedem Produkt zugewiesen ist, das in der Ladung enthalten ist. Weitere Informationen finden Sie unter [Kompatibilitätsgruppen für Gefahrstoffe](hazmat-setup.md#compatibility-groups).

Gehen Sie folgendermaßen vor, um die Kompatibilitätsprüfung auszuführen.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Ladungen**.
1. Wählen Sie eine Lieferung aus, um ihre Seite **Ladungsdetails** zu öffnen. (Sie können Ladungsdetails auch öffnen, indem Sie einen Link aus einer zugehörigen Lieferung auswählen.)
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Ladungen** in der Gruppe **Aktionen** die Option **Kompatibilitätsprüfung** aus.

Sie erhalten eine Nachricht, die Sie über die Ergebnisse der Prüfung informiert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]