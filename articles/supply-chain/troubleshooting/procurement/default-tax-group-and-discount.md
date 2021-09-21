---
title: Standardsteuergruppe und -skonto werden über das Rechnungskonto nicht ausgefüllt
description: Eine Standardsteuergruppe und ein Standardskonto werden über das Rechnungskonto nicht ausgefüllt.
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476437"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Standardsteuergruppe und -skonto werden über das Rechnungskonto nicht ausgefüllt

## <a name="symptoms"></a>Symptome

Wenn Sie ein vom Kundenkonto abweichendes Rechnungskonto verwenden, werden beim Erstellen einer Bestellung weder eine Standardsteuergruppe noch ein Standard-Skonto vom Rechnungskonto ausgefüllt.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Die Standardwerte für die Steuergruppe, Skonti und andere Preisinformationen basieren auf dem Kundenkonto und nicht auf dem Rechnungskonto.
