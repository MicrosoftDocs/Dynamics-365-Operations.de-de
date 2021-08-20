---
title: Die Kumulierung von Debitorenrückvergütungen schlägt fehl, wenn Artikelrückvergütungsgruppen verwendet werden
description: Wenn Sie Kundenrückvergütungsvereinbarungen in Kombination mit Artikelrückvergütungsgruppen verwenden, werden Rückvergütungen berechnet, die Kumulierung schlägt jedoch fehl.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760369"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Die Kumulierung von Debitorenrückvergütungen schlägt fehl, wenn Artikelrückvergütungsgruppen verwendet werden

KB-Nummer: 4611372

## <a name="symptoms"></a>Symptome

Wenn Sie Kundenrückvergütungsvereinbarungen (vom Typ *Betrag*) in Kombination mit Artikelrückvergütungsgruppen verwenden, werden Rückvergütungen berechnet, die Kumulierung schlägt jedoch fehl.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Artikelgruppen gruppieren nur Artikel, die dieselbe Schwellenwertbedingung haben. Die Rückvergütungsbedingung (Schwellenwert) wird gegen den Betrag für jeden Artikel und nicht gegen den kumulierten Betrag für einen Artikel in der Artikelgruppe festgelegt.
