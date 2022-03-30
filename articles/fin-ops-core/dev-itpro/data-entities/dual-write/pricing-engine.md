---
title: On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management
description: In diesem Thema wird die Verwendung des Preisgestaltungsmoduls in Microsoft Dynamics 365 Supply Chain Management über Microsoft Dynamics 365 Sales beschrieben.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6b0cc8f403be866ff00b89a33f6c59089c987bb0
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402829"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management enthält ein Preisgestaltungsmodul, das Handelsabkommen, Preislisten, Kundenbindungsprogramme, Werbeaktionen und Rabatte verwaltet. Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln. Wenn Sie duales Schreiben verwenden, verwenden Sie entweder die statische Preisgestaltung oder das Preisgestaltungsmodul von Supply Chain Management auf den Seiten **Angebot** und **Bestellung** in Microsoft Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Das Preisgestaltungsmodul von Supply Chain Management in Sales verwenden

1. Gehen Sie in Sales zu **Verkäufe \> Aufträge**.
1. Wählen Sie **Neu** aus, um einen neuen Auftrag zu erstellen, oder wählen Sie einen vorhandenen Auftrag in der Liste **Eigene Aufträge** aus.
1. Fügen Sie eine neue Auftragsposition hinzu.
1. Wenn Sie eine neue Bestellung erstellen, wählen Sie im Aktivitätsbereich **Preis für Auftrag** aus. Wenn Sie einen bestehenden Auftrag aktualisieren, wählen Sie Aktionsbereich **Neu berechnen** aus.
1. Die folgenden Spalten werden automatisch ausgefüllt:

    - Detailbetrag
    - Rabatt %
    - Rabatt
    - Vorfrachtbetrag
    - Frachtbetrag
    - Gesamtsteuer
    - Gesamtbetrag

> [!NOTE]
> Ein ähnlicher Prozess gilt, wenn Sie Angebote erstellen.

## <a name="how-it-works"></a>Funktionsweise

Wenn Sie einen Auftrag in Sales erstellen, wird dieser Auftrag sofort mit Supply Chain Management synchronisiert, indem die Werte verwendet werden, die Sie in Sales eingegeben haben. Wenn Sie **Preis für Auftrag** oder **Preisangebot** in Sales auswählen, berechnet Supply Chain Management den Preis für jede Auftragsposition und die Gesamtbestellung auf der Grundlage von Handelsvereinbarungsregeln, die in Supply Chain Management definiert sind. Die neu berechneten Werte werden dann wieder mit Sales synchronisiert.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Optionen zur Bewertung von Handelsvereinbarungen in Supply Chain Management festlegen

Sie können Supply Chain Management so konfigurieren, dass es Handelsvereinbarungen respektiert oder ignoriert, wenn es den Preis einer Bestellung berechnet, die in Sales erstellt wurde. Führen Sie zum Einrichten dieser Option die folgenden Schritte durch.

1. Melden Sie sich bei Ihrer Supply Chain Management-Umgebung an.
1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
1. Auf der **Preise**-Registerkarte auf dem **Handelsvereinbarungsauswertung**-Inforegister fügen Sie die Zeile für die **Manuelle Eingabe**-Richtlinie nach Bedarf hinzu oder entfernen Sie sie. Das Vorhandensein oder Nichtvorhandensein dieser Richtlinie steuert, ob das Supply Chain Management-Preisgestaltungsmodul automatisch den in Sales eingegebenen Verkaufspreis außer Kraft setzt.

    - Wenn die **Manuelle Eingabe**-Richtlinie *nicht* in der **Handelsvereinbarungsauswertung**-Einrichtung vorhanden ist, ist Supply Chain Management der Preismaster. Wenn ein Benutzer **Preis für Auftrag** oder **Preisangebot** im Aktivitätsbereich in Sales auswählt, wird das Preisgestaltungsmodul von Supply Chain Management aufgerufen, und der in Sales eingegebene Verkaufspreis wird überschrieben, es sei denn, er entspricht dem in Supply Chain Management berechneten Verkaufspreis.
    - Wenn die **Manuelle Eingabe**-Richtlinie in der *Handelsvereinbarungsauswertung*-Einrichtung vorhanden **ist**, ist Sales der Preismaster. Der in Sales eingegebene Verkaufspreis wird daran gehindert, automatisch überschrieben zu werden, wenn ein Benutzer **Preis für Auftrag** oder **Preisangebot** im Aktivitätsbereich von Sales auswählt.
    - Auftragspositionen und Angebotspositionen mit einem **Einzelpreis**- und/oder **Rabatt**-Wert von *0* (Null) in Sales werden als Sonderfall behandelt. Wenn ein relevanter Handelsvertragspreis verfügbar ist, wird Supply Chain Management es *immer* auf diese Felder anwenden, unabhängig von der **Handelsvereinbarungsauswertung**-Einrichtung.

    Ein Beispiel für jeden dieser Fälle finden Sie in den folgenden Szenarien.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Beispielszenario 1: Handelsvereinbarungsauswertung ohne Option „Manuelle Eingabe“

In diesem Szenario enthält die **Handelsvereinbarungsauswertung**-Einrichtung in Supply Chain Management *nicht* die **Manuelle Eingabe**-Richtlinie. Ein Sales-Benutzer gibt eine Auftragsposition mit einem Verkaufspreis ungleich null in Sales ein, und es ist kein Verkaufspreis für den Artikel in Supply Chain Management definiert.

1. In Sales erstellt ein Benutzer eine Auftragsposition mit einem **Einzelpreis**-Wert von 1 US-Dollar (USD).
1. Die Bestellposition wird mit Supply Chain Management mit einem Verkaufspreis von 1 USD synchronisiert.
1. In Sales wählt der Benutzer **Preis für Auftrag** im Aktivitätsbereich aus.
1. Supply Chain Management sucht nach relevanten Preisen und Rabatten und berechnet dann Summen. Da der Artikel in Supply Chain Management keinen Verkaufspreis hat, aktualisiert die Berechnung die Position, sodass sie einen Verkaufspreis von 0 USD hat.
1. Der neue Verkaufspreis der Position wird mit Sales synchronisiert.
1. Das Ergebnis ist eine Auftragsposition in Sales mit einem Verkaufspreis von 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Beispielszenario 2: Handelsvereinbarungsauswertung mit Option „Manuelle Eingabe“

Die **Handelsvereinbarungsauswertung**-Einrichtung in Supply Chain Management in diesem Szenario *enthält* die **Manuelle Eingabe**-Richtlinie. Ein Sales-Benutzer gibt eine Auftragsposition ein, die einen Verkaufspreis ungleich null in Sales hat. Supply Chain Management schließt eine Handelsvereinbarung ein, die einen Verkaufspreis von 2 USD für den bestellten Artikel festlegt.

1. In Sales erstellt ein Benutzer eine Auftragsposition für einen Artikel mit einem **Einzelpreis**-Wert von 1 USD.
1. Die Bestellposition wird mit Supply Chain Management mit einem Verkaufspreis von 1 USD synchronisiert.
1. In Sales wählt der Benutzer **Preis für Auftrag** im Aktivitätsbereich aus.
1. Weil die **Handelsvereinbarungsauswertung**-Einrichtung in Supply Chain Management die **Manuelle Eingabe**-Richtlinie umfasst, wird der Verkaufspreis nicht geändert, auch wenn eine geltende Handelsvereinbarung einen anderen Verkaufspreis festlegt.
1. Der Verkaufspreis bleibt in Sales und in Supply Chain Management unverändert.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Beispielszenario 3: Handelsvereinbarungsauswertung für einen Artikel mit einem Verkaufspreis von null in Sales

Die **Handelsvereinbarungsauswertung**-Einrichtung in Supply Chain Management in diesem Szenario *enthält* die **Manuelle Eingabe**-Richtlinie. Der Sales-Benutzer gibt eine Auftragsposition ein, die einen Verkaufspreis von 0 (null) in Sales hat. Supply Chain Management schließt eine Handelsvereinbarung ein, die einen Verkaufspreis von 2 USD für einen bestellten Artikel festlegt.

1. In Sales erstellt ein Benutzer eine Auftragsposition mit einem **Einzelpreis**-Wert von 0 USD und einem **Positionsrabatt**-Wert von 0 USD.
1. Die Bestellposition wird mit Supply Chain Management mit einem Verkaufspreis von 0 USD synchronisiert.
1. Da es eine Auftragsposition mit einem Verkaufspreis von 0 (Null) erhalten hat, ruft Supply Chain Management sein Preisgestaltungsmodul auf, obwohl die **Manuelle Eingabe**-Option aktiviert ist. Das Preisgestaltungsmodul gibt den Verkaufspreis von 2 USD zurück, der durch die Handelsvereinbarung festgelegt wird, und aktualisiert die Auftragsposition in Supply Chain Management.
1. Der aktualisierte Verkaufspreis ist noch nicht mit der Auftragsposition in Sales synchronisiert.
1. In Sales wählt der Benutzer **Preis für Auftrag** im Aktivitätsbereich aus.
1. Die Auftragsposition in Supply Chain Management behält ihren Verkaufspreis von 2 USD bei, der jetzt wieder mit Sales synchronisiert wird. Deshalb wird der **Einzelpreis**-Wert der Auftragsposition in Sales von 0 USD auf 2 USD aktualisiert.
1. In Sales gibt der Benutzer einen neuen **Positionsrabatt**-Wert von 0,50 USD ein. Sales berechnet nun, dass der **Erweiterter Betrag**-Wert für die Position 1,50 USD ist.
1. Die Bestellposition wird mit Supply Chain Management mit einem **Positionsrabatt**-Wert von 0,50 USD synchronisiert.
1. In Sales wählt der Benutzer **Preis für Auftrag** im Aktivitätsbereich aus.
1. Für die Auftragsposition ändern sich keine Preise oder Rabatte in Sales.

## <a name="limitations"></a>Einschränkungen

Wenn die Spalten in Sales ausgefüllt sind, gelten folgende Einschränkungen:

- Das Einrichten von Gebühren und Gebührenzuordnungen im Supply Chain Management wird in Sales nicht repliziert.
- Bei der Preisgestaltung werden keine speziellen Einzelhandelspreise berücksichtigt, die in der Spalte **Retail Channel** auf der Seite „Auftragsposition“ in Supply Chain Management angegeben sind.
- Rabatte, die im Abschnitt **Handelsvergütungsverwaltung** des Supply Chain Management definiert sind, werden nicht berücksichtigt.
- Die Preisgestaltung berücksichtigt keine Kaufverträge.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
