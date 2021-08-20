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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742027"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden

KB-Nummer: 4612803

## <a name="symptoms"></a>Symptome

Das Feld **Datum des letzten Tests** wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Das Datum des letzten Tests bezieht sich nicht auf Qualitätsprüfungsaufträge. Es speichert das Datum, an dem die Fertigartikel zum ersten Mal gekauft oder hergestellt wurde. Dieses Datum wird verwendet, um das Haltbarkeitsdatum zu berechnen.
