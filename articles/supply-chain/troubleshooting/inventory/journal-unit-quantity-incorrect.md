---
title: Die Einheit und die Stückzahl funktionieren in der Bestandserfassung nicht richtig.
description: Die Einheit und die Stückzahl funktionieren in der Bestandserfassung nicht richtig.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 074be71d7b6ec1acab6307a79e397c2a2a045c39
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778424"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Die Einheit und die Stückzahl funktionieren in der Bestandserfassung nicht richtig.

## <a name="symptoms"></a>Symptome

Bei der Arbeit mit Einheiten und Mengen in einer Bestandserfassung können eines oder beide der folgenden Probleme auftreten:

- Sie sehen keine Einheiten oder Stückzahlen in der Bestandserfassung, obwohl eine Umrechnungseinheit für das freigegebene Produkt eingerichtet ist, und Sie können die Einheit in der Bestandserfassung nicht ändern.
- Sie sehen die Felder **Menge** und **Einheit** in der Bestandserfassung, das Feld **Stückzahl** aber nicht. Wenn Sie die Einheit ändern, eine Menge eingeben und die Erfassung buchen, zeigt die Erfassung weiterhin die ursprüngliche Messung für diese Menge an.

## <a name="resolution"></a>Lösung

Führen Sie folgende Schritte aus, um dieses Problem zu beheben.

1. Stellen Sie im Arbeitsbereich **Funktionsverwaltung** sicher, dass die Funktion *Maßeinheit und Stückzahl in Bestandserfassungen* verwenden aktiviert ist. Diese Funktion fügt die Felder **Einheit** und **Stückzahl** zur Erfassung hinzu. (Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert.)
1. Verwenden Sie nach dem Einschalten der Funktion die Felder **Menge**, **Stückzahl** und **Einheit** wie folgt:

    - **Menge** – Geben Sie die Menge unter Verwendung der Standardeinheit an, die für das freigegebene Produkt definiert ist. Die Standardeinheit selbst wird hier jedoch nicht angezeigt. Wenn eine Umrechnung zwischen der Standardeinheit und der im Feld **Einheit** ausgewählten Einheit eingerichtet ist, wird das Feld **Menge** basierend auf der Auswahl in den Feldern **Stückzahl** und **Einheit** automatisch aktualisiert.
    - **Stückzahl** – Geben Sie die Menge unter Verwendung der Einheit an, die im Feld **Einheit** ausgewählt ist.
    - **Einheit** – Wählen Sie die Einheit aus, die auf den Wert im Feld **Stückzahl** angewendet werden soll.
