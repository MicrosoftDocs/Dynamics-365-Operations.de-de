---
title: Kanalspezifische Rabatte definieren
description: Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a23176cefde1f4d119828c9b124750d6106a3bfa
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019346"
---
# <a name="define-channel-specific-discounts"></a>Kanalspezifische Rabatte definieren

[!include [banner](includes/banner.md)]

Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.

## <a name="channel-specific-discounts"></a>Kanalspezifische Rabatte

Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dies kann erfolgen, um die lokalen Marktbedingungen anzusprechenoder mit einem konkurrierenden Einzelhändler in den Wettbewerb zu treten..

Retail verwendet Preisgruppen, um kanalspezifische Rabatte zu definieren. Preisgruppen können einer oder mehreren der folgenden Entitäten zugewiesen werden: Kanäle, Kataloge, Zugehörigkeiten und Treueprogramme. Dieser Artikel behandelt Kanäle. Aber die gleichen Konzepte gelten für Katalograbatte, Zugehörigkeitsrabatte und Treuerabatte.

## <a name="price-groups"></a>Preisgruppen

[![Preisgruppen](./media/price-groups-1024x608.png)](./media/price-groups.png)

Im Diagramm wird die Beziehung zwischen Entitäten dargelegt die auf einer Buchung (Kanal, Katalog, Zugehörigkeit, Debitor, Treuekarte) erscheinen und die verschiedenen Rabatttypen, die konfiguriert werden können. Alle Buchungen sind in einem Kanal vorhanden, daher ist sichergestellt, dass der Kanal in einer Buchung vorhanden ist. Die verbleibende Entitäten sind optional. Auf jeder Masterdaten Seite ist ein Link zu einer zugehörigen Preisgruppenseite, in der Sie Preisgruppen nach Bedarf anzeigen und hinzufügen können. Eine Preisgruppe wird verwendet, um vier unterschiedliche Arten Entitäten zu unterscheiden die auf Rabatte, Preisregulierungen und Handelsvereinbarungen angewendet werden soll. Es wird empfohlen, eine Strategie für die Planung zu erstellen, wie die Preisgruppen benannt werden sollen, um sie organisiert zu behalten. Eine Option wäre, einen Buchstaben oder eine Nummer als Präfix oder Suffix zu verwenden, um zwischen unterschiedlichen Arten zu unterscheiden. Beispiel 1 xxxxx für Kanalpreisgruppen und 2 xxxxx für Katalogpreisgruppen. Es gibt vier Abfrageseiten für die verschiedenen Einzelhandeltsentitäten für die Rabatten möglich sind.

- **Preisgruppen Retail Channel**- Diese Seite  enthält eine Liste der Kanäle und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
- **Katalogpreisgruppen**- Diese Seite enthält eine Liste der Kataloge und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
- **Treuepreisgruppen**- Diese Seite  enthält eine Liste der Treueprogramme und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
- **Zugehörigkeitspreisgruppen**- Diese Seite enthält eine Liste der Zugehörigkeiten und Rabatte, die für jede Preisgruppe verknüpft sind.

## <a name="example-channel-discount-set-up"></a>Beispieleinrichtung für Kanalrabatte

Das folgende Beispiel veranschaulicht die Aufgaben zur Einrichtung von Kanalrabatten.

1. In vorliegenden Beispiel haben Sie einen  Kanal namens **Houston** und erstellen einen neuen Rabatt namens **Zurück zur Schule**.
2. Da die Preisgestaltungs- und Rabattstrategie die Möglichkeit von Kanalrabatten umfasst, erstellen Sie immer eine kanalspezifische Preisgruppe, wenn Sie einen Kanal erstellen.
3. Sie haben die Preisgruppe **Houston-PG** und diese ist dem Kanal **Houston** zugewiesen.
4. Nachdem Sie den neuen Rabatt **Zurück zur Schule** erstellt haben, müssen Sie auf **Preisgruppen** oben auf der Seite **Rabatt** klicken. Die **Rabattpreisgruppen**-Seite wird geöffnet. Danach klicken Sie auf **Neu** und wählen die Preisgruppe **Houston-PG** aus.
5. Jetzt können Sie den Rabatt aktivieren und für den Kanal umsetzen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Preisregulierungen und Rabatte](price-adjustments-discounts.md)
