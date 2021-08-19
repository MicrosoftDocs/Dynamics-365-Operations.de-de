---
title: Problembehandlung bei Verkaufsangeboten
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 92b77c1b7de1f5c946e677c810c0d0e43427473e7ba26679df23f7663946dbc0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765393"
---
# <a name="troubleshoot-sales-quotations"></a>Problembehandlung bei Verkaufsangeboten

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Ich kann die Verkaufsmenge eines Verkaufsangebots für einen Serviceartikel nicht ändern.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie versuchen, eine Verkaufsmenge (**SalesQty**-Feld) für einen Artikel vom Typ *Dienstleistung* auf einer Verkaufsangebotsposition festzulegen, wird die folgende Meldung angezeigt: „Aktualisierung für Feld Menge nicht zulässig.“

### <a name="issue-resolution"></a>Problemlösung

Sie können keine Verkaufsmenge für Produkte festlegen, bei denen es sich um Serviceartikel handelt. Wenn Sie beispielsweise einen Service zum Installieren eines Artikels anbieten, ist es nicht sinnvoll, eine Menge zu erfassen, da kein physischer Artikel vorhanden ist. Es gibt nur einen Service.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]