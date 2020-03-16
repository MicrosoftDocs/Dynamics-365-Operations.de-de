---
title: Optionen zur Sperrung von Rabatten für Einzelhandelsprodukte
description: Es gibt verschiedene Ursachen, warum Einzelhändler mehrere Produkte nicht als ermäßigt anzeigen wollen, entweder während einer Aktion oder während des Verkaufs am Point-of-Sale.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6a683ffce487dc4388711ad160c2e8dc55a690dd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057463"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Optionen zur Sperrung von Rabatten für Einzelhandelsprodukte

[!include [banner](includes/banner.md)]

Es gibt verschiedene Ursachen, warum Einzelhändler mehrere Produkte nicht als ermäßigt anzeigen wollen, entweder während einer Aktion oder während des Verkaufs am Point-of-Sale.

Die folgenden Optionen, die auf der Registerkarte **Commerce** aus freigegebenen Produkten gefunden werden können, ermöglichen es zu verhindern, alle oder manuell Rabatte zu konfigurieren. Die Einstellungen können auch auf der Ebene der Kategorie aus der Kategoriehierarchie heraus angegeben werden.

- **Sperren Sie Alle Rabatte**: Wählen Sie diese Option aus, um alle Arten Rabatte, die angewendet werden können, für dieses Produkt zu verhindern. Dazu zählen Aktionen wie Angebots-Sortiment, Mengen und Schwellenwertrabatte sowie manuelle Positions- und Buchungsrabatte, die im Zuge eines Verkaufs von einem POS-Benutzer angewendet werden.
- **Sperren Sie manuelle Rabatte**: Wählen Sie diese Option, um manuelle Positions- oder Buchungsrabatte nur zu verhindern, die im Rahmen eines Verkaufs von einem POS-Benutzer angewendet werden. Produkte mit dieser Option, die ausgewählt werden, stehen für Aktionen, wie Mischungs- und Abgleichungs- und Menge und Schwellenwertrabatte immer noch zur Verfügung.

> [!NOTE]
> Hinweis: Diese Einstellungen schränken nicht den Preisüberschreibungsarbeitsgang ein, da dieses den Basispreis festlegt und Rabatt nicht behandelt werden. .

[![Rabattfeld verhindern](./media/prevent-discounts.png)](./media/prevent-discounts.png)
