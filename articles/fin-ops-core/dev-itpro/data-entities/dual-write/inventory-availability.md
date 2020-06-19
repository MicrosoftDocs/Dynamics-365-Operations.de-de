---
title: Inventarverfügbarkeit in dualem Schreiben
description: Dieses Thema bietet Informationen über das Prüfen der Bestandverfügbarkeit in dualem Schreiben.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426981"
---
# <a name="inventory-availability"></a>Verfügbarkeit des Bestands

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Mithilfe der Bestandverfügbarkeit können Sie Ihr Inventar überprüfen, bevor Sie ein Produkt zu den Formularen **Zitate**, **Aufträge** oder **Rechnungen** in modellgesteuerten Apps in Dynamics 365 hinzufügen. Zum Beispiel ist die Überprüfung des Inventars und die Bestimmung eines Erfüllungstermins eine Schlüsselaufgabe im [Aussicht auf Bargeld](dual-write-prospect-to-cash.md) Prozess. Wenn Sie nicht über genügend Bestandr verfügen, können Sie einen Liefertermin basierend auf den projizierten Bestandeinnahmen und -Problemen schätzen. Sie können auch die ATP-Informationen des Produkts überprüfen, in denen Sie die ATP-Menge im vordefinierten Zeitrahmen finden.

## <a name="on-hand-inventory"></a>Verfügbarer Bestand 

In der Kopfzeile des Formales **Angebote**, **Aufträge**, oder **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt. Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen und das Produkt angeben können, für das Sie den Lagerbestand überprüfen möchten. Es gibt die Bestandinformationen von Dynamics 365 Supply Chain Management zurück und zeigt die gleichen Informationen wie [Lagerbestand](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Die Informationen enthalten diese Mengen:

- **Verfügbare Menge**
- **Verfügbare Menge in Reserve**
- **Verfügbare Menge**
- **Bestellte Menge**
- **Auftragsmenge**
- **Reservierte bestellte Menge**
- **Insgesamt verfügbare Menge**

## <a name="atp-information"></a>VfZ-Informationen

Bei Zeilenartikeln in den Formularen **Angebote**, **Aufträge**, oder **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt. Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen, Produkt, Lagerstandort, Lagerbestand und bestellte Menge angeben können.. Es gibt die **VIZ-Informationen** aus dem Supply Chain Management zurück und zeigt die Einstellungen, die in [vielversprechende Bestellung](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) beschrieben sind. Die Informationen umfassen **VfZ-Menge**, **Belegmenge**, **Ausgabemenge**, und **Verfügbare Menge**.
