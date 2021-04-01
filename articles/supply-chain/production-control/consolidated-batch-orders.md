---
title: Konsolidierte Chargenaufträge
description: Dieser Artikel beschreibt das Konzept der konsolidierten Chargenaufträgen.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed722ba0c79afa038f1af7b4491f3ff18b052067
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246380"
---
# <a name="consolidated-batch-orders"></a>Konsolidierte Chargenaufträge

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt das Konzept der konsolidierten Chargenaufträgen.

Ein produzierter Sammelartikel wird als übergeordneter Artikel angesehen, und ein verpackter Artikel ist ein untergeordneter Artikel. Die Beziehung zwischen dem Sammelartikel und dem verpackten Artikel wird in einer Konvertierung von Sammelartikeln ausgedrückt. Diese Konvertierung von Sammelartikeln wird im Sammelartikel selbst definiert.  

Verpackte Artikel können Containern entweder der gleichen Größe oder mit mehreren Größen verpackt werden, die als eine Einheit eingestuft werden. Indem Sie die Aufträge für einen Sammelartikel konsolidieren, können Sie alle zugehörigen Chargenaufträge in einer einzigen Ansicht anzeigen, mit deren Hilfe Sie noch verbleibende Arbeit leichter ermitteln können.  

Ein konsolidierter Chargenauftrag kann eine beliebige Kombination der folgenden Aufträge enthalten:

-   Einzelner Sammelauftrag und mehrere Verpackungsaufträge
-   Mehrere Sammelaufträge und mehrere Verpackungsaufträge
-   Mehrere Sammelaufträge und ein einzelner Verpackungsauftrag
-   Nur Verpackungsaufträge






[!INCLUDE[footer-include](../../includes/footer-banner.md)]