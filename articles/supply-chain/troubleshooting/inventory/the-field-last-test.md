---
title: Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden
description: Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026552"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden

KB-Nummer: 4612803

## <a name="symptoms"></a>Symptome

Das Feld **Datum des letzten Tests** wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Das Datum des letzten Tests bezieht sich nicht auf Qualitätsprüfungsaufträge. Es speichert das Datum, an dem die Fertigartikel zum ersten Mal gekauft oder hergestellt wurde. Dieses Datum wird verwendet, um das Haltbarkeitsdatum zu berechnen.
