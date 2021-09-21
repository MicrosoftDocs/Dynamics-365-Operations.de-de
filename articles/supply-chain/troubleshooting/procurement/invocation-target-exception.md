---
title: Eine Ausnahme tritt während der Kreditorenrechnungsbuchung auf.
description: Die Ausnahme „Ausnahme wurde vom Ziel eines Aufrufs ausgelöst" tritt während der Kreditorenrechnungsbuchung auf.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476440"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>Eine Ausnahme tritt während der Kreditorenrechnungsbuchung auf.


## <a name="symptoms"></a>Symptome

Bei der Buchung einer Kreditorenrechnung erhalten Sie folgende Ausnahme:

> Ausnahme wurde vom Ziel eines Aufrufs ausgelöst

## <a name="cause"></a>Ursache

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

## <a name="resolution"></a>Lösung

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
