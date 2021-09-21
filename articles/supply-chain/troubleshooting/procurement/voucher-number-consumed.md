---
title: Eine Produktzugangs-Belegnummer wird auch dann verbraucht, wenn kein Beleg generiert wird
description: Eine Produktzugangs-Belegnummer wird verbraucht, auch dann, wenn während des Produktzugangs kein Finanzbeleg generiert wird
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
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476438"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Eine Produktzugangs-Belegnummer wird auch dann verbraucht, wenn kein Beleg generiert wird

## <a name="symptoms"></a>Symptome

Eine Produktzugangs-Belegnummer wird verbraucht, auch wenn während des Produktzugangs kein Finanzbeleg generiert wird.

## <a name="resolution"></a>Lösung

Wenn die **Verbindlichkeiten bei Produktzugang abgrenzen**-Option für die Artikelmodellgruppe auf *Nein* festgelegt ist, werden keine Buchungen im Hauptbuch vorgenommen. Ein physisches Ereignis wird jedoch zum Zwecke der Abrechnung in einem Nebenbuch aufgezeichnet, und für dieses Ereignis ist eine Belegnummer erforderlich. Diese Belegnummer ist die Belegnummer, auf die in den Bestandstransaktionen verwiesen wird.

Wir empfehlen Ihnen, die **Verbindlichkeiten bei Produktzugang abgrenzen**-Option auf *Ja* festzulegen, wie im folgenden Blogbeitrag beschrieben: [Sonstige Zuschläge zum Zeitpunkt des Produktzugangs buchen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
