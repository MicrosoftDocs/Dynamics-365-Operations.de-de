---
title: Artikel über mehrere Debitorenaufträge und Rechnungen zurückgeben
description: In diesem Thema werden die Funktionen erläutert, um Rücklieferungen über mehrere Debitorenaufträgen und Rechnungen in Dynamics 365 Commerce zu ermöglichen.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 410a78dca29f1d723a5b5ef43836d07ec5502a567ec81098241fafeb6354373b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770980"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikel über mehrere Debitorenaufträgen und Rechnungen zurückgeben

[!include [banner](includes/banner.md)]


Rücklieferungen können über mehrere Aufträge und Rechnungen erfolgen. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Commerce konfigurieren, um Rücklieferungen für mehrere Debitorenaufträge und Rechnungen zu unterstützen

1. Wechseln Sie zu **Handelsparameter \> Debitorenaufträge**.
1. Aktivieren Sie den Parameter **Rücklieferungen für mehrere Aufträge aktivieren**. 

## <a name="process-returns"></a>Rücklieferungen verarbeiten

Nachdem der Parameter aktiviert und die Änderungen mit den Shops synchronisiert wurden, kann der Kassierer im Shop mehrere Aufträge für einen Debitor zur Rücklieferung auswählen.

Wenn die Aufträge ausgewählt werden, wird eine Liste aller retournierbaren Produkte für alle Rechnungen des Auftrags angezeigt. Der Kassierer kann dann die Produkte auswählen, die retourniert werden sollen. Es wird ein einzelner Rücklieferungsauftrag für alle ausgewählten Produkte erstellt.
