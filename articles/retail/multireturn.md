---
title: Artikel über mehrere Debitorenaufträgen und Rechnungen zurückgeben
description: In diesem Thema werden die Funktionen erläutert, um Rücklieferungen über mehrere Debitorenaufträgen und Rechnungen in Microsoft Dynamics 365 for Retail zu ermöglichen.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517073"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikel über mehrere Debitorenaufträgen und Rechnungen zurückgeben

[!include [banner](includes/banner.md)]


In Version 10.0 von Dynamics 365 for Finance and Operations können Rücklieferungen mehrere Aufträge und Rechnungen übergreifend vorgenommen werden, während in Versionen vor 10.0 Rücklieferungen nur für eine einzelne Rechnung verarbeitet werden konnten. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Retail konfigurieren, um Rücklieferungen für mehrere Debitorenaufträge und Rechnungen zu unterstützen

1. Wechseln Sie zu **Retail-Parameter \> Debitorenaufträge**.
1. Aktivieren Sie den Parameter **Rücklieferungen für mehrere Aufträge aktivieren**. 

## <a name="process-returns"></a>Rücklieferungen verarbeiten

Nachdem der Parameter aktiviert und die Änderungen mit den Shops synchronisiert wurden, kann der Kassierer im Shop mehrere Aufträge für einen Debitor zur Rücklieferung auswählen.

Wenn die Aufträge ausgewählt werden, wird eine Liste aller retournierbaren Produkte für alle Rechnungen des Auftrags angezeigt. Der Kassierer kann dann die Produkte auswählen, die retourniert werden sollen. Es wird ein einzelner Rücklieferungsauftrag für alle ausgewählten Produkte erstellt.
