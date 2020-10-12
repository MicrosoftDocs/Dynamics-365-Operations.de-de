---
title: Problembehandlung bei Verkaufsangeboten
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834361"
---
# <a name="troubleshoot-sales-quotations"></a>Problembehandlung bei Verkaufsangeboten

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Ich kann die Verkaufsmenge eines Verkaufsangebots für einen Serviceartikel nicht ändern.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie versuchen, eine Verkaufsmenge (**SalesQty**-Feld) für einen Artikel vom Typ *Dienstleistung* auf einer Verkaufsangebotsposition festzulegen, wird die folgende Meldung angezeigt: „Aktualisierung für Feld Menge nicht zulässig.“

### <a name="issue-resolution"></a>Problemlösung

Sie können keine Verkaufsmenge für Produkte festlegen, bei denen es sich um Serviceartikel handelt. Wenn Sie beispielsweise einen Service zum Installieren eines Artikels anbieten, ist es nicht sinnvoll, eine Menge zu erfassen, da kein physischer Artikel vorhanden ist. Es gibt nur einen Service.

