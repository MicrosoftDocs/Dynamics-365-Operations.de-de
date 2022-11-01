---
title: Neuberechnung von Zeilen-Nettobeträgen beim Import von Verkaufsaufträgen und Angeboten
description: Dieser Artikel beschreibt, ob und wie das System Zeilen-Nettobeträge neu berechnet, wenn Verkaufsaufträge und Angebote importiert werden. Außerdem wird erläutert, wie Sie das Verhalten in verschiedenen Versionen von Microsoft Dynamics 365 Supply Chain Management steuern können.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719333"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Neuberechnung von Zeilen-Nettobeträgen beim Import von Verkaufsaufträgen und Angeboten

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, ob und wie das System Zeilen-Nettobeträge neu berechnet, wenn Verkaufsaufträge und Angebote importiert werden. Außerdem wird erläutert, wie Sie das Verhalten in verschiedenen Versionen von Microsoft Dynamics 365 Supply Chain Management steuern können.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Wie Aktualisierungen der Positionsnettobeträge beim Import berechnet werden

Supply Chain Management Version 10.0.23 hat den [Bugfix 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) eingeführt. Mit diesem Bugfix wurden die Bedingungen geändert, unter denen das Feld **Nettobetrag** einer Zeile aktualisiert oder neu berechnet werden kann, wenn Aktualisierungen von bestehenden Verkaufsaufträgen und Angeboten importiert werden. In Version 10.0.29 können Sie diesen Bugfix ersetzen, indem Sie die Funktion *Positionsnettobetrag beim Importieren berechnen* einschalten. Diese Funktion hat einen ähnlichen Effekt, bietet jedoch eine globale Einstellung, mit der Sie bei Bedarf zum alten Verhalten zurückkehren können. Obwohl das neue Verhalten das System intuitiver arbeiten lässt, kann es in bestimmten Szenarien, in denen alle der folgenden Bedingungen erfüllt sind, zu unerwarteten Ergebnissen führen:

- Daten, die vorhandene Datensätze aktualisieren, werden über die Entität *Auftragspositionen V2*, *Verkaufsangebotspositionen V2* oder *Rücklieferungspositionen* mithilfe von Open Data Protocol (OData) importiert, einschließlich Situationen, in denen Sie duales Schreiben, Importieren/Exportieren über Excel und einige Integrationen von Drittanbietern verwenden.
- Geltende [Bewertungsrichtlinien für Handelsabkommen](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) legen eine Änderungsrichtlinie fest, die Aktualisierungen im Feld **Nettobetrag** in Auftragspositionen, Verkaufsangebotspositionen und/oder Rücklieferungspositionen einschränkt. Beachten Sie, dass bei Zeilen für Rücklieferungen das Feld **Nettobetrag** immer berechnet wird und nicht manuell festgelegt werden kann.
- Die importierten Daten enthalten Änderungen im Feld **Nettobetrag** in Positionen oder Änderungen (wie Stückpreis, Menge oder Rabatt), die dafür sorgen, dass der Wert des Felds **Nettobetrag** in Positionen für einen oder mehrere bestehende Positionsdatensätze neu berechnet wird.

In diesen spezifischen Szenarien hat die Bewertungsrichtlinie für Handelsabkommen die Folge, dass Aktualisierungen des Felds **Nettobetrag** auf der Position mit Einschränkungen belegt werden. Diese Einschränkung wird als *Änderungsrichtlinie* bezeichnet. Wenn Sie das Feld über die Benutzeroberfläche bearbeiten oder neu berechnen, werden Sie aufgrund dieser Richtlinie vom System aufgefordert, zu bestätigen, ob Sie die Änderung vornehmen möchten. Wenn Sie jedoch einen Datensatz importieren, muss das System die Auswahl für Sie treffen. Vor Version 10.0.23 hat das System den Nettobetrag der Position immer unverändert gelassen, es sei denn, der Nettobetrag der eingehenden Position war 0 (null). In neueren Versionen aktualisiert oder berechnet das System den Nettobetrag jedoch immer nach Bedarf, es sei denn, es wird ausdrücklich angewiesen, dies nicht zu tun. Obwohl das neue Verhalten logischer ist, kann es Ihnen Probleme bereiten, wenn Sie bereits Prozesse oder Integrationen ausführen, die das ältere Verhalten zeigen. Dieser Artikel beschreibt, wie Sie bei Bedarf zum alten Verhalten zurückkehren können.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Die Berechnungen der Positionsnettobeträge in den Versionen 10.0.29 und höher steuern

Supply Chain Management Version 10.0.29 führte eine Funktion mit dem Namen *Positionsnettobetrag beim Importieren berechnen* ein. Diese Funktion fügt eine Option mit dem Namen **Positionsnettobetrag berechnen** zur Seite **Debitorenkontoparameter** hinzu. Mit dieser Option können Sie zwischen dem neuen und dem alten Verhalten für die Berechnung der Positionsnettobeträge beim Importieren wählen.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Die Funktion „Positionsnettobetrag beim Importieren berechnen“ ein- oder ausschalten

Wenn Sie auf Version 10.0.29 aktualisieren, ist die Funktion *Positionsnettobetrag beim Importieren berechnen* standardmäßig aktiviert, und die neue Option **Positionsnettobetrag berechnen** ist zunächst auf *Ja* gestellt. Die Einstellung *Ja* entspricht dem neuen Standardverhalten. Es entspricht dem Systemverhalten, wenn die Funktion ausgeschaltet ist, außer im Fall der Funktionalität des [CalculateLineAmount-Parameters](#CalculateLineAmount), wie später in diesem Artikel beschrieben. Die Einstellungen *Nein* entspricht dem Systemverhalten vor Version 10.0.23 und wird hauptsächlich bereitgestellt, um Legacy-Integrationsszenarien zu unterstützen.

Administratoren können die Funktion *Positionsnettobetrag beim Importieren berechnen* mithilfe des [Arbeitsbereichs für die Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein- oder ausschalten.

### <a name="set-the-calculate-line-net-amount-option"></a>Die Option „Positionsnettobetrag beim Importieren berechnen“ festlegen

Wenn die Funktion *Positionsnettobetrag beim Importieren berechnen* eingeschaltet ist, können Sie die Option **Positionsnettobetrag berechnen** mit diesen Schritten festlegen.

1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
1. Legen Sie in der Registerkarte **Preise** auf dem Inforegister **Berechnung des Positionsnettobetrag durch Integration** die Option **Positionsnettobetrag berechnen** auf einen der folgenden Werte fest:

    - *Ja*: Das System berechnet und aktualisiert die Positionsbeträge bei Bedarf immer neu. (Daher wird die Bewertungsrichtlinie für Handelsabkommen ignoriert.)
    - *Nein*: Wenn der vorhandene oder eingehende Nettobetrag für eine Position 0 (null) ist, wird der Wert für diese Position basierend auf anderen Werten (z. B. Einzelpreis, Menge und Rabatt) neu berechnet. Wenn der vorhandene oder eingehende Nettobetrag von 0 (null) abweicht und eine Änderungsrichtlinie auf das Feld **Nettobetrag** in der Position gesetzt wird, wird das Feld nicht neu berechnet oder aktualisiert, selbst wenn eingehende Änderungen am Positionspreis, der Menge und/oder dem Rabatt bedeuten würden, dass der Positionsbetrag eigentlich neu berechnet werden sollte. Dieses Verhalten entspricht dem von Version 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>Wie sich die Funktion „Positionsnettobetrag beim Importieren berechnen“ auf den CalculateLineAmount-Parameter auswirkt

Wenn die Funktion *Positionsnettobetrag beim Importieren berechnen* eingeschaltet ist, wirkt sich der Wert des `CalculateLineAmount`-Parameters für die `SalesLine`- und `SalesQuotationLine`-Tabellen nicht aus. Stattdessen wird das Verhalten global durch die Option **Positionsnettobetrag berechnen** gesteuert, die im vorherigen Abschnitt beschrieben wurde. Wenn die Funktion aktiviert ist, dürfen Sie daher keine Abhängigkeit aus dem `CalculateLineAmount`-Wert übernehmen.

Wenn die Funktion *Positionsnettobetrag beim Importieren berechnen* ausgeschaltet ist, funktioniert der `CalculateLineAmount`-Parameter für die `SalesLine`- und `SalesQuotationLine`-Tabellen wie in den Versionen 10.0.23 bis 10.0.28 von Supply Chain Management, wie im nächsten Abschnitt beschrieben.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Positionsnettobetragsberechnungen in den Versionen 10.0.28 und höher steuern

Seit der [Bugfix 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) in Version 10.0.23 eingeführt wurde kann ausgewählt werden, wie sich jede relevante Datenentität verhalten soll, wenn ein Positionsnettobetrag bearbeitet wird oder aufgrund anderer Änderungen (z. B. eines aktualisierten Artikelpreises) neu berechnet werden muss. Sie können dieses Verhalten steuern, indem Sie den neuen `CalculateLineAmount`-Parameter für jede Position auf einen der folgenden Werte in der importierten Datei festlegen:

- **`CalculateLineAmount` = *1***: Das Feld **Nettobetrag** auf der Position wird immer neu berechnet und aktualisiert, unabhängig davon, ob eine Änderungsrichtlinie für das Feld festgelegt ist und unabhängig vom Wert des eingehenden oder vorhandenen Positionsnettobetrags.
- **`CalculateLineAmount` = *0***: Wenn der vorhandene oder eingehende Nettobetrag für eine Position 0 (null) ist, wird der Wert für diese Position basierend auf anderen Werten (z. B. Einzelpreis, Menge und Rabatt) neu berechnet. Wenn der vorhandene oder eingehende Nettobetrag von 0 (null) abweicht und eine Änderungsrichtlinie auf dem Feld **Nettobetrag** auf der Position festgelegt ist, wird das Feld nicht neu berechnet oder aktualisiert.  

Das Systemverhalten hängt von Ihrer Version von Supply Chain Management ab:

- In Version 10.0.22 und früher verhält sich das System immer so, als ob `CalculateLineAmount` auf *0* eingestellt wäre, und es gibt keine Möglichkeit, dafür zu sorgen, dass sie sich so verhält, als wäre `CalculateLineAmount` auf *1* gesetzt.
- In den Versionen 10.0.23 bis 10.0.28 verhält sich das System so, als wäre `CalculateLineAmount` für alle Positionen auf *1* gestellt, wenn sie in der Importdatei nicht explizit auf *0* festgelegt ist.
