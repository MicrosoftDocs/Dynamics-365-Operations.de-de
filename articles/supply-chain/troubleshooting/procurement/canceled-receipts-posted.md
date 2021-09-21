---
title: Transaktionen können auf ein gesperrtes Sachkonto gebucht werden
description: Wenn ein Produktzugang storniert wird, können Transaktionen auf gesperrte Sachkonten gebucht werden, obwohl die Hauptkonten gesperrt sind
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
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476492"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Transaktionen können auf ein gesperrtes Sachkonto gebucht werden

## <a name="symptoms"></a>Symptome

Wenn ein Produktzugang storniert wird, können Transaktionen auf gesperrte Sachkonten gebucht werden, obwohl die Hauptkonten gesperrt sind.

## <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Stellen Sie auf der **Lieferantenparameter**-Seite auf der Registerkarte **Allgemeines** sicher, dass die **Produktzugang auf Sachkonto buchen**-Option auf *Ja* festgelegt ist.
1. Erstellen Sie eine Bestellung und fügen Sie eine Bestellposition mit einer Menge von *1.000* für ein Produkt hinzu.
1. Bestätigen Sie die Bestellung.
1. Buchen Sie den Produktzugang und überprüfen Sie die Gutscheine.
1. Sperren Sie die relevanten Hauptkonten *200140* und *140200*.
1. Stornieren Sie den gebuchten Produktzugang.
1. Beachten Sie, dass Transaktionen auf die gesperrten Sachkonten gebucht werden können.

## <a name="resolution"></a>Lösung

Transaktionen können auf die gesperrten Sachkonten gebucht werden, wenn Produktbelege storniert werden, da dieses Verhalten korrekte Buchungen ermöglicht.
