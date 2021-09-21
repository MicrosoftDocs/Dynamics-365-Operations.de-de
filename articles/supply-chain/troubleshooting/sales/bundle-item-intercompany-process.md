---
title: Bündelartikel wird in einem Intercompany-Prozess nicht unterstützt
description: Der Bündelartikel kann nicht gekauft werden. Der Auftrag kauft nur die Komponenten des Bündelartikels, nicht den Bündelartikel selbst.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476446"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Ein Bündelartikel wird in einem Intercompany-Prozess nicht unterstützt

## <a name="symptoms"></a>Symptome

Der Bündelartikel ist für die Bestellung nicht verfügbar, da Sie bei Prüfung der Auftragspositionen für den Bündelartikel feststellen werden, dass die Menge *0* (Null) und der Status *Storniert* ist.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Der Auftrag kauft nur die Komponenten des Bündelartikels. Der Bündelartikel selbst wird nicht gekauft. Wenn Sie ein Bündel kaufen müssen, prüfen Sie, ob Sie es als Bündelartikel markieren müssen, da diese Funktion für Szenarien zur Umsatzrealisierung konzipiert ist. Weitere Informationen zu Bündelartikeln finden Sie unter [Bündel](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
