---
title: Kanalspezifische Rabatte definieren
description: Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieser Artikel prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.industry: Retail
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
ms.openlocfilehash: f426503a6897a73010b77082f4277b65545bfcc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273553"
---
# <a name="define-channel-specific-discounts"></a>Kanalspezifische Rabatte definieren

[!include [banner](includes/banner.md)]

Dieser Artikel prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.

## <a name="channel-specific-discounts"></a>Kanalspezifische Rabatte

Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dies kann erfolgen, um die lokalen Marktbedingungen anzusprechen oder mit konkurrierenden Einzelhändlern in den Wettbewerb zu treten.

Commerce verwendet Preisgruppen, um kanalspezifische Rabatte zu definieren. Preisgruppen können einer oder mehreren der folgenden Entitäten zugewiesen werden: Kanäle, Kataloge, Zugehörigkeiten und Treueprogramme. Dieser Artikel behandelt Kanäle. Aber die gleichen Konzepte gelten für Katalograbatte, Zugehörigkeitsrabatte und Treuerabatte.

## <a name="price-groups"></a>Preisgruppen

[![Preisgruppen.](./media/price-groups-1024x608.png)](./media/price-groups.png)

Im Diagramm wird die Beziehung zwischen Entitäten dargelegt die auf einer Buchung (Kanal, Katalog, Zugehörigkeit, Debitor, Treuekarte) erscheinen und die verschiedenen Rabatttypen, die konfiguriert werden können. Alle Buchungen sind in einem Kanal vorhanden, daher ist sichergestellt, dass der Kanal in einer Buchung vorhanden ist. Die verbleibende Entitäten sind optional. Auf jeder Masterdaten Seite ist ein Link zu einer zugehörigen Preisgruppenseite, in der Sie Preisgruppen nach Bedarf anzeigen und hinzufügen können. Eine Preisgruppe wird verwendet, um vier unterschiedliche Arten Entitäten zu unterscheiden die auf Rabatte, Preisregulierungen und Handelsvereinbarungen angewendet werden soll. Es wird empfohlen, eine Strategie für die Planung zu erstellen, wie die Preisgruppen benannt werden sollen, um sie organisiert zu behalten. Eine Option wäre, einen Buchstaben oder eine Nummer als Präfix oder Suffix zu verwenden, um zwischen unterschiedlichen Arten zu unterscheiden. Beispiel 1 xxxxx für Kanalpreisgruppen und 2 xxxxx für Katalogpreisgruppen. Es gibt vier Abfrageseiten für die verschiedenen Commerce-Entitäten für die Rabatten möglich sind.

- **Kanal Channel-Preisgruppen**– Diese Seite enthält eine Liste der Kanäle und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
- **Katalogpreisgruppen**- Diese Seite enthält eine Liste der Kataloge und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
- **Treuepreisgruppen**- Diese Seite enthält eine Liste der Treueprogramme und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
- **Zugehörigkeitspreisgruppen**- Diese Seite enthält eine Liste der Zugehörigkeiten und Rabatte, die für jede Preisgruppe verknüpft sind.

## <a name="example-channel-discount-set-up"></a>Beispieleinrichtung für Kanalrabatte

Das folgende Beispiel veranschaulicht die Aufgaben zur Einrichtung von Kanalrabatten.

1. In vorliegenden Beispiel haben Sie einen Kanal namens **Houston** und erstellen einen neuen Rabatt namens **Zurück zur Schule**.
2. Da die Preisgestaltungs- und Rabattstrategie die Möglichkeit von Kanalrabatten umfasst, erstellen Sie immer eine kanalspezifische Preisgruppe, wenn Sie einen Kanal erstellen.
3. Sie haben die Preisgruppe **Houston-PG** und diese ist dem Kanal **Houston** zugewiesen.
4. Nachdem Sie den neuen Rabatt **Zurück zur Schule** erstellt haben, müssen Sie auf **Preisgruppen** oben auf der Seite **Rabatt** klicken. Die **Rabattpreisgruppen**-Seite wird geöffnet. Danach klicken Sie auf **Neu** und wählen die Preisgruppe **Houston-PG** aus.
5. Jetzt können Sie den Rabatt aktivieren und für den Kanal umsetzen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Preisregulierungen und Rabatte](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
