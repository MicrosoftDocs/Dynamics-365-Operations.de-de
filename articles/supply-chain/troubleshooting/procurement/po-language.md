---
title: Bestellungen spiegeln nicht die Spracheinstellungen der juristischen Person wider
description: Der Produktname einer Bestellung wird in der Systemsprache anstelle der Sprache angezeigt, die für die juristische Person festgelegt wurde, in der die Bestellung erstellt wurde
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476433"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Bestellungen spiegeln nicht die Spracheinstellungen der juristischen Person wider


## <a name="symptoms"></a>Symptome

Der Produktname einer Bestellung wird in der Systemsprache anstelle der Sprache angezeigt, die für die juristische Person festgelegt wurde, in der die Bestellung erstellt wurde.

## <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Stellen Sie die Systemsprache auf *EN-US* (Amerikanisches Englisch) ein.
1. Stellen Sie sicher, dass es ein Produkt gibt, in dem die *EN-US* und *DE* (Deutschland)-Sprachen für die Übersetzung des Produktnamens gepflegt werden.
1. Ändern Sie die Sprache einer juristischen Person in *DE*.
1. In der juristischen Person, in der *DE* als Sprache festgelegt ist, erstellen Sie eine Bestellung, die das Produkt enthält.
1. Beachten Sie, dass der Produktname weiterhin in US-Englisch (der Systemsprache) angezeigt wird.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Bei Bestellungen wird das Produkt immer in der Systemsprache angezeigt. Die Bestellsprache wird verwendet, wenn ein Bestätigungsjournal erstellt wird.
