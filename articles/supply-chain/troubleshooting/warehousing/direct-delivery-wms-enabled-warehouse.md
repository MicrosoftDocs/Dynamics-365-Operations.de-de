---
title: Direktlieferung kann für WMS-fähigen Lagerort nicht verarbeitet werden.
description: Wenn für den Lagerort WMS aktiviert ist, unterstützt es keine direkte Lieferung. Um die direkte Lieferung zu verwenden, müssen Sie ein Element und einen Lagerort auswählen, die nicht zu WMS gehören.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476496"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Direktlieferung kann für WMS-fähigen Lagerort nicht verarbeitet werden.

## <a name="symptoms"></a>Symptome

Wenn ein Artikel einer Auftragsposition für die Direktlieferung aus einem Lagerort hinzugefügt wird, der für die Lagerortverwaltung (WMS) aktiviert ist, erhalten Sie beim Aktualisieren der Auftragsposition die folgende Fehlermeldung:

> Die Direktlieferung kann für Lagerort 1% nicht verarbeitet werden, da die Lagerortverwaltung aktiviert ist. Bitte geben Sie einen anderen Lagerort an, für den die Lagerortverwaltung nicht aktiviert ist.

## <a name="resolution"></a>Lösung

Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Derzeit unterstützt WMS die direkte Lieferung nicht. Um die direkte Lieferung zu verwenden, müssen Sie daher ein Element und ein Lagerort auswählen, die nicht zu WMS gehören.
