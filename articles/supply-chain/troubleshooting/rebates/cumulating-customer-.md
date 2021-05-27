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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026531"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Die Kumulierung von Debitorenrückvergütungen schlägt fehl, wenn Artikelrückvergütungsgruppen verwendet werden

KB-Nummer: 4611372

## <a name="symptoms"></a>Symptome

Wenn Sie Kundenrückvergütungsvereinbarungen (vom Typ *Betrag*) in Kombination mit Artikelrückvergütungsgruppen verwenden, werden Rückvergütungen berechnet, die Kumulierung schlägt jedoch fehl.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Artikelgruppen gruppieren nur Artikel, die dieselbe Schwellenwertbedingung haben. Die Rückvergütungsbedingung (Schwellenwert) wird gegen den Betrag für jeden Artikel und nicht gegen den kumulierten Betrag für einen Artikel in der Artikelgruppe festgelegt.
