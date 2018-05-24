---
title: "Auflösung einer Stücklistenversion"
description: "In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 80c9fa6ec98bd2cdc3edd5329e2a619ef9cc8cb2
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="explosion-of-a-bom-version"></a>Auflösung einer Stücklistenversion

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.

Eine Bedarfsauflösung einer Stücklistenversion erstellt einen Bedarf für jeden Stücklistenpositionsartikel an einem bestimmten Standort (und ggf. in einem bestimmten Lager). In einer standortspezifischen Stückliste kann ein bestimmtes Lager für jede Stücklistenposition definiert werden. Zudem bestimmen die Dimensionseinstellungen des Artikels für jede Stücklistenposition, ob das Lager erforderlich ist. Der resultierende Bedarf für jeden Stücklistenpositionsartikel wird dann Ausgangspunkt für weitere Bedarfsauflösungen. Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist obligatorisch und muss in die Bedarfsbuchung eingegeben werden.
-   Die Standortdimension ist einheitlich. Aus diesem Grund handelt es sich bei dem Standort für geringen Bedarf um den Standort, der auch in der anfänglichen Bedarfsbuchung enthalten ist.

In der folgenden Illustration ist der Ablauf der Bedarfsauflösung für die Produktprogrammplanung dargestellt. ![Bedarfsauflösung – Verwenden einer Stücklistenversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Produktprogrammplanungslauf - Ermittlung der Stücklistenversion](master-plan-bom-version-determined.md)

[Produktprogrammplanung und Funktion für mehrere Standorte](master-plan-multisite-functionality.md)




