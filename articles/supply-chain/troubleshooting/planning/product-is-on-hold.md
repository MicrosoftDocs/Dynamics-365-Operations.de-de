---
title: Produkt liegt für Transaktionen in Wartestellung
description: Nachdem Sie Planungsaufträge fixiert haben, erhalten Sie eine Nachricht, die besagt, dass ein Element für Transaktionen zurückgestellt ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301278"
---
# <a name="product-is-on-hold-for-transactions"></a>Produkt liegt für Transaktionen in Wartestellung

Fehlercode: SYS13295

## <a name="symptoms"></a>Symptome

Nachdem Sie geplanter Aufträge fixiert haben, erhalten Sie die folgende Fehlermeldung:

> Artikel '%1' gesperrt für Buchungen in '%2'.

## <a name="cause"></a>Ursache

Bei der Beschreibung von gesperrten Artikeln verwendet das System die Begriffe *gesperrt*, *gestoppt* und *gehalten* austauschbar. Dieser Fehler bedeutet, dass das Element in seinen Standardauftragseinstellungen als **Gestoppt** festgelegt ist.

Wenn ein Element gesperrt ist und Sie es zu einer Bestell- oder Verkaufsauftragszeile hinzufügen, erhalten Sie eine Warnmeldung. Wenn ein Element gesperrt ist, können Bestandstransaktionen, die sich auf die Bestell- oder Verkaufsauftragszeile beziehen, nicht geändert werden (z. B. wenn Sie einen Lieferschein oder eine Rechnung buchen). Sie können einen gekauften Artikel sperren und gleichzeitig den Artikel verkaufen. In diesem Fall ist das Kontrollkästchen **Gestoppt** auf einer Bestellung aktiviert, aber der Artikel ist nicht im Bestand oder auf einem Verkaufsauftrag gesperrt.

Hier sind einige der Bedingungen, die dazu führen können, dass eine Artikelnummer für den Verkauf gesperrt wird:

- Das Element befindet sich noch in der Entwicklung oder Herstellung. Sie möchten daher nicht, dass er verkauft oder reserviert wird.
- Sie haben viele fehlerhafte Elemente erhalten, und die Fehler müssen behoben werden, bevor das Element verkauft werden kann.

In Fällen dieser Art können Sie das Element sperren, bis das Problem behoben ist.

Wenn ein Element gesperrt ist und Sie eine Zeile für die Rücklieferung erstellen, erhalten Sie eine Nachricht. Sie können eine Serie oder ein Los eines Elements nicht sperren. Wenn Teile eines Elements gesperrt werden müssen, können Sie sie durch Verschieben des Bestands oder durch Sperren des gesamten Bestands des Elements für diesen Zeitraum sperren.

## <a name="resolution"></a>Lösung

- Öffnen Sie die Seite **Standardauftragseinstellungen** für das Element, und deaktivieren Sie das Kontrollkästchen **Stopp**.
