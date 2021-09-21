---
title: Aktualisierungskonflikt, wenn als Bestandsbewertungsmethode entweder „Standardkosten“ oder „Gleitender Durchschnitt“ verwendet wird
description: Ein Aktualisierungskonflikt tritt auf, wenn als Bestandsbewertungsmethode entweder „Standardkosten“ oder „Gleitender Durchschnitt“ verwendet wird
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476474"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Ein Aktualisierungskonflikt tritt auf, wenn als Bestandsbewertungsmethode entweder „Standardkosten“ oder „Gleitender Durchschnitt“ verwendet wird

## <a name="symptoms"></a>Symptome

Wenn Sie Dokumente wie Bestandserfassungen, Einkaufsrechnungen oder Auftragsrechnungen aus Gründen der Skalierbarkeit und Leistung parallel buchen, wird möglicherweise eine Fehlermeldung zu einem Aktualisierungskonflikt angezeigt und einige der Dokumente werden möglicherweise nicht gebucht. Dieses Problem kann auftreten, wenn als Bestandsbewertungsmethode entweder *Standardkosten* oder *Gleitender Durchschnitt* verwendet wird. Beide Methoden sind kontinuierliche Nachkalkulationsmethoden. Anders ausgedrückt: Die endgültigen Kosten werden zum Zeitpunkt der Buchung festgelegt.

Wenn Sie die Methode *Gleitender Durchschnitt* verwenden, ähnelt die Fehlermeldung diesem Beispiel:

> Bestandswert xx.xx wird nach Berechnung der anteiligen Ausgaben nicht erwartet

Wenn Sie die Methode *Standardkosten* verwenden, ähnelt die Fehlermeldung diesem Beispiel:

> Die Standardkosten stimmen nicht mit dem Wert des finanziellen Bestands nach der Aktualisierung überein. Wert = xx.xx, Menge = yy.yy, Standardkosten = zz.zz

## <a name="workaround"></a>Problemumgehung

Verwenden Sie die folgenden Problemumgehungen, bis Microsoft eine Lösung zur Behebung des Problems veröffentlicht, um diese Fehler zu vermeiden oder zu reduzieren:

- Buchen Sie die fehlgeschlagenen Dokumente erneut.
- Erstellen Sie Dokumente mit weniger Positionen.
- Vermeiden Sie Dezimalwerte in den Standardkosten. Versuchen Sie, die Standardkosten so zu definieren, dass das Feld **Preismenge** auf *1* festgelegt ist. Wenn Sie einen Wert für **Preismenge** angeben müssen, der größer als *1* ist, versuchen Sie, die Anzahl der Dezimalstellen in den Standardkosten der Einheit zu minimieren. (Idealerweise sollten weniger als zwei Dezimalstellen vorhanden sein.) Vermeiden Sie beispielsweise die Definition von Standardkosteneinstellungen wie **Preis** = *10* und **Preismenge** = *3*, weil sie Standardkosten pro Einheit von 3,333333 erzeugen (wobei sich der Dezimalwert wiederholt).
- Vermeiden Sie in den meisten Dokumenten mehrere Positionen mit derselben Kombination aus Produkt- und Finanzbestandsdimensionen.
- Reduzieren Sie den Parallelisierungsgrad. (In diesem Fall wird Ihr System möglicherweise schneller, da weniger Aktualisierungskonflikte und Wiederholungsversuche auftreten.)
