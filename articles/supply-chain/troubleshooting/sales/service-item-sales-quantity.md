---
title: Serviceelementmenges in einer Angebotsposition kann nicht festgelegt werden
description: Bei der Arbeit mit Angeboten können Sie keine Verkaufsmenge für Produkte festlegen, die Serviceartikel sind, da keine physischen Artikel zu zählen sind.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476485"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Die Verkaufsmenge eines Serviceartikels in einer Angebotsposition kann nicht geändert werden.

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Verkaufsmenge (**SalesQty**-Feld) für einen Artikel vom Typ *Dienstleistung* auf einer Verkaufsangebotsposition festzulegen, wird die folgende Meldung angezeigt:

> Aktualisierung für Feld Menge nicht zulässig.

## <a name="cause"></a>Ursache

Dieses Verhalten ist beabsichtigt. Sie können keine Verkaufsmenge für Produkte festlegen, bei denen es sich um Serviceartikel handelt. Wenn Sie beispielsweise einen Service zum Installieren eines Artikels anbieten, ist es nicht sinnvoll, eine Menge zu erfassen, da kein physischer Artikel zum Zählen vorhanden sind. Es gibt nur einen Service.
