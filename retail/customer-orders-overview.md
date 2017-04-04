---
title: "Debitorenauftragsüberblick"
description: "Dieses Thema enthält Informationen zu modernem Debitorenaufträge in KleinPOS (MPOS). Debitorenaufträge sind auch Sonderauftrag. Das Thema enthält eine Diskussion zu zugehörigen Parameter und Buchungsflüsse."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Debitorenauftragsüberblick

Dieses Thema enthält Informationen zu modernem Debitorenaufträge in KleinPOS (MPOS). Debitorenaufträge sind auch Sonderauftrag. Das Thema enthält eine Diskussion zu zugehörigen Parameter und Buchungsflüsse.

In einer OmniKanalkleinwelt stellen viele Einzelhändler von Debitorenaufträgen die Option oder aus Sonderauftrag verschiedene, Produkt- und Erfüllungsbedingungen zu decken bereit. Nachfolgend sind einige typische Szenarios:

-   Ein Debitor fordert Produkte für eine bestimmten Adresse an einem bestimmten Datum geliefert werden.
-   Ein Debitor möchte Produkte von einem Shop oder einem Lagerplatz aufheben, der aus Filiale oder vom Lagerplatz abweicht, dem der Debitor die Produkte gekauft hat.
-   Ein Debitor fordert einer anderen Person Produkte aufheben, die der Debitor erworben.

Einzelhändler können auch Debitorenaufträge, verlorenen Verkäufe zu minimieren, den vordefinierten Ausfälle möglicherweise nicht anzeigen, da die Waren zu unterschiedlichen Zeiten oder an einem Ort geliefert oder verarbeitet werden kann.

## <a name="set-up-customer-orders"></a>Einstellungsdebitorenaufträge
Nachfolgend sind einige der Parameter, die auf die Einzelhandelsparameter ** ** Seite festgelegt werden können, um festzulegen, z Debitorenaufträge erfüllt werden:

-   ** Standardeinzahlungsprozentsatz ** - Geben Sie den Betrag, den der Debitor bezahlen muss z eine Einzahlung zusammensetzt, bevor ein Auftrag bestätigt werden kann. Der Standardeinzahlungsbetrag wird als Prozentsatz des Auftragswerts berechnet. Abhängig von Rechten kann ein Shop zuordnen in der Lage, den Betrag zu überschreiben, indem sie verwendet Einzahlungsaußerkraftsetzung ** **.
-   ** Annullierungsgebührprozentsatz ** – Wenn ein Zuschlag angewendet wird, wenn ein Kundenauftrag zurückgezogen wurde, geben Sie den Betrag dieses Zuschläge an.
-   ** Annullierungsgebührcode ** – Wenn ein Zuschlag angewendet wird, wenn ein Kundenauftrag zurückzuziehen, dieser Belastung wird auf einen Zuschlagscode im Auftrag in Microsoft Dynamics AX angezeigt. Verwenden Sie diesen Parameter, um den Annullierungsgebührcode zu definieren.
-   ** Versandkostencode ** - Einzelhändler kann eine Zuschlagsgebühr für den Versand von Waren an einen Debitor erheben. Der Betrag wird auf Versandkosten dieser einen Zuschlagscode im Auftrag in Dynamics AX angezeigt. Verwenden Sie diesen Parameter, um den Versandkostencode den Versandkosten im Kundenauftrag zuzuordnen.
-   ** Rückerstattungsversandkosten ** - gibt an, ob Versandkosten, die einem Kundenauftrag zugeordnet werden, rückvergütbar sind.
-   ** Maximaler Betrag ohne Genehmigung ** – wenn Versandkosten rückvergütbar sind, geben den Höchstbetrag der Versandkostenrückerstattungen über Rücklieferungen anzeigen. Wenn dieser Betrag überschritten wird, ist Manageraußerkraftsetzung erforderlich, der für die Rückerstattung fortzusetzen. Um die folgenden Szenarien zu gewährleisten, kann eine Gebührenerstattung Versandkosten den Betrag für überschreiten der ursprünglich geleistete:
    -   Zuschläge sind auf die Stufe im Auftragskopf und übernommen, wenn eine beliebige Menge einer Produktgruppe zurückgegeben wird, kann die Gebührenerstattung maximale Versandkosten, die für die Produkte und die Menge darf, nicht auf Weise bestimmt werden, die für alle Stellen bearbeitet.
    -   Versandkosten werden für jede Instanz zur Versand- verursacht. Wenn Debitorenrücklieferungsprodukte mehrmals und die Richtlinie des Einzelhändlers angibt, an dem der Einzelhändler die Kosten von Rückholversandkosten werden, sind die Rückholversandkosten höchstens der tatsächlichen Versandkosten.

## <a name="transaction-flow-for-customer-orders"></a>Buchungsfluss für Kundenaufträge
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Erstellen eines modernem Kundenauftrag in KleinPOS

1.  Dient zum Hinzufügen eines Debitors zur Buchung.
2.  Hinzufügen von Produkten zum Einkaufskorb hinzufügen.
3.  ** Auf Erstellen Kundenauftrag ** und wählen dann den Auftragstyp aus. Der Auftragstyp kann entweder ** Kundenauftrag ** oder ** Angebot **.
4.  ** Versand- auf aktiviert ** oder ** versenden Sie alle ** die Produkte für eine Adresse im Feld Debitorenkonto zu versenden, geben das angeforderte Versanddatum und geben Versandkosten an.
5.  ** Auf Entnahme Sie oben ausgewählt ** ** oder nehmen Sie auf ** Produkte auswählen, die vom aktuellen Shops oder aus einem anderen Shop an einem bestimmten Datum verarbeitet werden.
6.  Sie Treiben den Einzahlungsbetrag ein, wenn eine Einzahlung zusammensetzt erforderlich ist.

### <a name="edit-an-existing-customer-order"></a>Bearbeiten eines Bestandskundeauftrag

1.  Auf der Startseite klicken Sie suchen ** ** Sie einen Auftrag.
2.  Suchen und wählen Sie den zu bearbeitenden Auftrag aus. Am unteren Seitenrand klicken Sie auf ** Bearbeiten **.

### <a name="pick-up-an-order"></a>Markieren Sie einen Auftrag erstellen

1.  Auf der Startseite klicken Sie suchen ** ** Sie einen Auftrag.
2.  Wählen Sie den Auftrag aus, aufzuheben. Am unteren Seitenrand klicken Sie ** Entnahme und Verpackung **.
3.  ** Auf Erhöht ** auf.

### <a name="cancel-an-order"></a>Ziehen eines Auftrag storniert

1.  Auf der Startseite klicken Sie suchen ** ** Sie einen Auftrag.
2.  Wählen Sie den Auftrag aus zu stornieren. Am unteren Seitenrand ** auf Abbrechen **.

#### <a name="create-a-return-order"></a>Erstellen einer Rücklieferung

1.  Auf der Startseite klicken Sie suchen ** ** Sie einen Auftrag.
2.  Wählen Sie den Auftrag aus zurückkehren möchten, wählen Sie die Rechnung für den Auftrag aus, und wählen Sie dann die für die Produktgruppe aus, um Waren zurückzukehren.
3.  Am unteren Seitenrand klicken Sie auf Zurück ** **.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchroner Buchungsfluss für Kundenaufträge
Debitorenaufträge können vom Verkaufsstelle (POS)- Kunden entweder im synchronen Modus oder in asynchronen Modus erstellt werden.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivieren Sie im Modus asynchronen Debitorenaufträge, erstellt werden

1.  In Dynamics AX ** klicken Sie Einzelhandel und Handel ** &gt; ** auf installierten Kanal ** &gt; ** POS eingerichtet ** &gt; ** POS-Profil ** &gt; ** Funktionsprofile **.
2.  Wählen Sie im Inforegister ** Allgemein ** Legen Sie die erstellen ** Kundenauftrag Sie in async Modus ** Option fest ** Ja **.

Wenn die im Kundenauftrag ** erstellen Sie async Modus ** Option auf festgelegt ** Ja **, werden Debitorenaufträge immer in asynchronen Modus erstellt, wenn Retail Transaction Service (RTS) verfügbar ist. Wenn Sie diesen Option ** no **, Debitorenaufträge immer im Modus synchronen erstellt werden, indem RTS verwendet. Wenn im Modus Debitorenaufträge asynchronen erstellt werden, werden sie in Dynamics AX mittels Einzelvorgänge des Pulles (P) abgerufen und eingefügt. Die entsprechenden Aufträge werden in Dynamics AX erstellt, wenn Sie Aufträge ** synchronisieren ** entweder manuell oder durch eine Stapelverarbeitung ausgeführt wird.

<a name="see-also"></a>Siehe auch
--------

[Hybride Debitorenaufträge] (hybrid-customer-orders.md)


