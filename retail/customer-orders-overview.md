---
title: "Anzeigen der Kundenaufträge"
description: "Dieses Thema enthält Informationen zu Bestellungen in n Retail Modern POS (MPOS). Debitorenaufträge sind auch Sonderauftrag. Das Thema enthält eine Diskussion zu zugehörigen Parametern und Buchungsflüssen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e96579437ab59e99268263a51fc589eaacb98cc1
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="customer-orders-overview"></a>Anzeigen der Kundenaufträge

[!include[banner](includes/banner.md)]


Dieses Thema enthält Informationen zu Bestellungen in n Retail Modern POS (MPOS). Debitorenaufträge sind auch Sonderauftrag. Das Thema enthält eine Diskussion zu zugehörigen Parametern und Buchungsflüssen.

In einer Omni-Channel-Welt stellen viele Einzelhändler von Debitorenaufträgen als Option oder Sonderaufträge, um die verschiedenen Produkt- und Erfüllungsbedingungen zu erfüllen. Nachfolgend sind einige typische Szenarios:

-   Ein Debitor fordert, dass Produkte für eine bestimmten Adresse an einem bestimmten Datum geliefert werden.
-   Ein Debitor möchte Produkte von einem Shop oder einem Lagerplatz aufheben, der aus Filiale oder vom Lagerplatz abweicht, an dem der Debitor die Produkte gekauft hat.
-   Ein Debitor fordert einer anderen Person auf, Produkte aufzuheben, die der Debitor erworben.

Einzelhändler können auch Debitorenaufträge verwenden, um verlorenen Verkäufe zu minimieren, den vordefinierten Ausfälle möglicherweise nicht anzeigen, da die Waren zu unterschiedlichen Zeiten oder an einem Ort geliefert oder verarbeitet werden kann.

## <a name="set-up-customer-orders"></a>Debitorenbestellungen einrichten
Nachfolgend sind einige der Parameter, die auf der Seite e **Einzelhandelsparameter** eingerichtet sind, um zu definiueren, wie Debitorenaufträge erfüllt werden:

-   **Standardanzahlung in Prozent** –  Geben Sie den Betrag, den der Debitor bezahlen muss ein als eine Anzahlung, bevor ein Auftrag bestätigt werden kann. Der Standardanzahlungsbetrag wird als Prozentsatz der Summe des Auftragswerts berechnet. Abhängig von Rechten kann ein Shopmitarbeiter den Betrag überschreiben, indem er**Anzahlung überschreiben verwendet**. 
-   **Annullierungsgebührprozentsatz** – Wenn ein Zuschlag angewendet wird, wenn ein Kundenauftrag zurückgezogen wurde, geben Sie den Betrag dieses Zuschlages an.
-   **Annullierungsgebührcode** – Wenn ein Zuschlag angewendet wird, wenn ein Kundenauftrag zurückgezogen wird, wird diese Belastung auf einen Zuschlagscode im Auftrag von Microsoft Dynamics AX angezeigt. Verwenden Sie diesen Parameter, um den Annullierungsgebührcode zu definieren.
-   **Versandkostencode** ** - Einzelhändler können eine Zuschlagsgebühr für den Versand von Waren an einen Debitor erheben. Der Betrag wird auf Versandkosten dieser unter einem Zuschlagscode im Auftrag von Dynamics AX angezeigt. Verwenden Sie diesen Parameter, um den Versandkostencode den Versandkosten im Kundenauftrag zuzuordnen.
-   **Rückerstattungsversandkosten**  – Gibt an, ob Versandkosten, die einem Kundenauftrag zugeordnet werden, rückvergütbar sind.
-   **Maximaler Betrag ohne Genehmigung** – wenn Versandkosten rückvergütbar sind, geben den Höchstbetrag der Versandkostenrückerstattungen über Rücklieferungen anzeigen. Wenn dieser Betrag überschritten wird, ist eine Manageraußerkraftsetzung erforderlich, um die Rückerstattung fortzusetzen. Um die folgenden Szenarien zu gewährleisten, kann eine Gebührenerstattung der Versandkosten den Betrag  überschreiten, der ursprünglich geleistet wurde:
    -   Zuschläge werden auf Ebene Auftragsüberschrift angewendet und wenn eine beliebige Menge einer Produktgruppe zurückgegeben wird, kann die Gebührenerstattung für die maximalen Versandkosten, die für die Produkte und die Menge zugelassen ist nicht für alle Einzelhandelskunden gleich angewendet werden.
    -   Versandkosten werden für jede Versandinstanz erhoben. Wenn ein Kunde Produkte mehrmals zurücksendet und die Richtlinie des Einzelhändlers angibt, dass der Einzelhändler die Kosten für den Rückversand übernimmt, dann sind die Rückholversandkosten höher als die tatsächlichen Versandkosten.

## <a name="transaction-flow-for-customer-orders"></a>Transaktionsfluss für Kundenbestellungen
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Debitorenauftrag im Retail Modern POS erstellen

1.  Dient zum Hinzufügen eines Debitors zur Buchung.
2.  Produkte zum Warenkorb hinzufügen
3.  Klicken Sie auf **Kundenauftrag erstellen** und wählen Sie dann den Auftragstyp aus. Der Auftragstyp kann entweder **Kundenauftrag** oder **Angebot** sein.
4.  Klicken Sie auf **Versand aktivier** oder  **Alle versenden**, um die Produkte für eine Adresse im Feld Debitorenkonto zu versenden, geben das angeforderte Versanddatum und geben die Versandkosten an.
5.  Klicken Sie auf **Ausgewählte entnehmen** oder **Alle entnehmen**, um die Produkte auswählen, die vom aktuellen Shop oder aus einem anderen Shop an einem bestimmten Datum verarbeitet werden.
6.  Fordern Sie den Anzahlungsbetrag ein, wenn eine Anzahlung erforderlich ist.

### <a name="edit-an-existing-customer-order"></a>Bearbeiten eines bestehenden Kundenauftrags.

1.  Auf der Startseite klicken Sie auf**Bestellung suchen**. 
2.  Suchen und wählen Sie den zu bearbeitenden Auftrag aus. Klicken Sie unten auf der Seite auf **Bearbeiten**.

### <a name="pick-up-an-order"></a>Einen Auftrag entnehmen

1.  Auf der Startseite klicken Sie auf**Bestellung suchen**. 
2.  Wählen Sie den Auftrag aus, der gewählt werden soll. Klicken Sie unten auf der Seite auf **Bearbeiten und verpacken**.
3.  Klicken Sie auf **Abholen**.

### <a name="cancel-an-order"></a>Stornieren einer Auftragsposition

1.  Auf der Startseite klicken Sie auf**Bestellung suchen**. 
2.  Wählen Sie den Auftrag aus, der storniert werden soll. Klicken Sie unten auf der Seite auf **Abbrechen**.

#### <a name="create-a-return-order"></a>Erstellen einer Rücklieferung

1.  Auf der Startseite klicken Sie auf**Bestellung suchen**. 
2.  Wählen Sie den Auftrag aus, zu dem Sie zurückkehren möchten, wählen Sie die Rechnung für den Auftrag aus, und wählen Sie dann die Produktgruppe aus, um zu den Waren zurückzukehren.
3.  Klicken Sie unten auf der Seite auf **Zur Bestellung zurückkehren**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchroner Transaktionsfluss für Kundenbestellungen
Debitorenaufträge können von den Verkaufsstellen (POS)-Kunden entweder im synchronen Modus oder im asynchronen Modus erstellt werden.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivieren Sie Kundenaufträge, um diese im asynchronen Modus zu erstellen

1.  Klicken Sie in Dynamics AX auf **Einzelhandel und Handel** &gt; **Kanaleinstellung** &gt; **POS-Einstellung** &gt; **POS-Profil** &gt; **Funktionsprofile**.
2.  Wählen Sie im Inforegister **Allgemein** unter **Kundenauftrag in asynchronem Modus erstellen** die Option **Ja** aus.

Wenn die Option **Kundenauftrag in asynchronem Modus** auf **Ja** gesetzt ist, werden Debitorenaufträge immer in asynchronen Modus erstellt, selbst wenn Retail Transaction Service (RTS) verfügbar ist. Wenn Sie diesen Option auf **Nein** setzen, werden Debitorenaufträge immer im Modus synchronen mithilfe von RTS erstellt. Wenn Debitorenaufträge asynchronen erstellt werden, werden sie in Dynamics AX mittels Pulles (P)-Aufträge abgerufen. Die entsprechenden Aufträge werden in Dynamics AX erstellt, wenn **Aufträge synchronisieren** entweder manuell oder mithilfe von Chargenaufträgen ausgeführt wird.

<a name="see-also"></a>Siehe auch
--------

[Hybrid-Kundenaufträge](hybrid-customer-orders.md)




