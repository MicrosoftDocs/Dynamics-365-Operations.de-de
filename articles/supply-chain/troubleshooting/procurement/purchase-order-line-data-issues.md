---
title: Abweichungen bei Bestellpositionsdaten
description: Sie sehen Datenabweichungen oder Datenbeschädigungen in Ihren Bestellpositionen.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100802"
---
# <a name="purchase-order-line-data-discrepancies"></a>Abweichungen bei Bestellpositionsdaten

## <a name="symptoms"></a>Symptome

Wenn Sie die Positionen einer Bestellung prüfen, stellen Sie eines oder mehrere der folgenden Probleme fest:

- Es gibt eine Datenabweichung oder -beschädigung in den Restmengen der Bestellpositionen (Lieferung oder Rechnung).
- Eine Bestellposition oder ein Kopfzeilenstatus ist beschädigt.
- Sie können eine Bestellung nicht abrechnen, weil Sie beispielsweise eine oder mehrere der folgenden Fehlermeldungen erhalten:

    - „Gestoppt (Fehler): Transaktion wurde bereits gebucht.“
    - „Die Menge kann nicht in Rechnungs gestellt werden, da Lagerbuchungen mit dem Status ‚Eingegangen‘ unzureichend sind.“
    - „Unzureichende Bestandsbuchungen mit dem Status ‚Gekauft‘ für Artikel %0 Menge %1.“

- Sie können eine Bestellung beispielsweise aufgrund eines der folgenden Probleme nicht abschließen oder schließen:

    - Die Schaltfläche **Abschließen** ist nicht verfügbar.
    - Sie können die bestellte Menge einer Bestellposition für eine Bestellung nicht stornieren, die sich in einem bestätigten und erhaltenen Zustand befindet.

## <a name="cause"></a>Ursache

Diese Probleme werden normalerweise durch beschädigte Daten oder eine Diskrepanz in den Restmengen für eine oder mehrere Bestellpositionen verursacht.

## <a name="resolution"></a>Lösung

Sie können diese Probleme normalerweise wie im folgenden Verfahren beschrieben beheben, indem Sie den Einkaufsstatus, verbleibende Liefermengen und/oder verbleibende Rechnungsmengen für die relevanten Bestellpositionen aktualisieren.

1. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigung \> Bestellpositionen manuell korrigieren**.
1. Suchen Sie im Feld **Bestellung** nach der Bestellung, die Ihnen Probleme bereitet, und wählen Sie sie aus.
1. Wählen Sie im Abschnitt **Bestellpositionen** eine Position aus, in der Sie eine Abweichung gefunden haben.
1. Überprüfen Sie im Abschnitt **Lagerbuchung** die angezeigten Daten. Wenn Sie Inkonsistenzen zwischen einer Bestellposition und ihren Lagerbuchungen feststellen, wählen Sie einen der folgenden Befehle im Aktivitätsbereich aus, je nachdem, wo Sie die Inkonsistenzen sehen:

    - **Neu berechnen \> Verbleibende Liefermengen neu berechnen**: Aktualisiert automatisch den Bestellpositions- und Kopfzeilenstatus. Diese Funktion funktioniert nur für gelagerte Bestellpositionen (d. h. Positionen, bei denen der Artikel ein Lagerartikel ist). Nicht-Lagerartikel und Artikel mit Artikelgewicht werden derzeit nicht unterstützt.
    - **Neu berechnen \> Verbleibende Rechnungsmengen neu berechnen**: Aktualisiert automatisch den Bestellpositions- und Kopfzeilenstatus. Diese Funktion funktioniert nur für gelagerte Bestellpositionen (d. h. Positionen, bei denen der Artikel ein Lagerartikel ist). Nicht-Lagerartikel und Artikel mit Artikelgewicht werden derzeit nicht unterstützt.
    - **Neu berechnen \> Status neu berechnen**: Der Status der ausgewählten Position wird neu berechnet. Diese Berechnung basiert auf der bestehenden Logik. Daher wird der Kopfzeilenstatus der Bestellung nach Bedarf basierend auf dem neuen Bestellpositionsstatus aktualisiert.

1. Sollten Sie dennoch Inkonsistenzen in den Restmengen sehen, können Sie diese bei Bedarf über folgende Felder direkt bearbeiten:

    - Rest liefern
    - Lager-Restlieferungsmenge
    - Rechnungsrestmenge
    - Lagerrechnungs-Restmenge
