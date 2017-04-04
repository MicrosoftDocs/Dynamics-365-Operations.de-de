---
title: Kanalspezifische Rabatte definieren
description: "Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Kanalspezifische Rabatte definieren

Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen. 

<a name="channel-specific-discounts"></a>Kanalspezifische Rabatte
--------------------------

Einzelhändler bilden häufig verschiedene Rabatte in verschiedenen Kanälen angezeigt. Dies ist für den lokalen Marktlagen der Adresse erfolgen oder möglicherweise von konkurrierende Einzelhändler.

Einzelhandel und Handel in Microsoft Dynamics 365 für Arbeitsgänge verwendet Preisgruppen, um Kanalbesondererabatte zu definieren. Preisgruppen können einer oder mehreren der folgenden Entitäten zugewiesen werden: Kanäle, Kataloge, Zugehörigkeiten und Treueprogramme. Dieser Artikel behandelt Kanäle. Aber die gleichen Konzepte gelten für Katalograbatte, Zugehörigkeitsrabatte und Treuerabatte.

## <a name="price-groups"></a>Preisgruppen
\[id= Beschriftung "\_"align= Anhang 256084 " alignnone" width= " 640 "\]![Preisgruppen ([]. /media/price-groups-1024x608.png)]". /media/price-groups.png) Verknüpft Klein-__ent_dict_PLACEHOLDER Preisgruppe für\[/caption

Im Diagramm wird veranschaulicht die Beziehung zwischen Entitäten, die auf eine Buchung (Kanal, Katalog, Zugehörigkeit, Debitor, Treuekarte) und verschiedenen Rabatttypen sind, die konfiguriert werden können. Alle Buchungen werden in einem Kanal auf, daher wird der Kanal wird sichergestellt, um nach einer Buchung vorhanden sein. Die verbleibende Entitäten sind optional. Auf jeder Masterdaten Seite ist ein Link zu einer zugehörigen Preisgruppenseite, in der Sie Preisgruppen nach Bedarf anzeigen und hinzufügen können. Bei einer Preisgruppe wird verwendet, um vier unterschiedliche Arten Entitäten auf Rabatte, den und Preisregulierungen auf Handelsvereinbarungen zugeordnet werden soll. Es wird empfohlen, eine Strategie für Planung, wie der Name die Preisgruppen sie organisiert beibehalten. Eine Option wird, einen Buchstaben oder eine Nummer präfix oder Suffix zu verwenden sein, um zwischen unterschiedlichen Arten zu unterscheiden. Beispiel 1 xxxxx für Kanalpreisgruppen und 2 xxxxx für Katalogpreisgruppen. Es gibt vier Abfrageseiten für die verschiedenen Einzelhandeltsentitäten für die Rabatten möglich sind.

-   **Preisgruppen Retail Channel **- Diese Seite enthält eine Liste der Kanäle und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
-   **Katalogpreisgruppen **- Diese Seite enthält eine Liste der Kataloge und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
-   **Treuepreisgruppen **- Diese Seite enthält eine Liste der Treueprogramme und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.
-   **Zugehörigkeitspreisgruppen **- Diese Seite enthält eine Liste der Zugehörigkeiten und Rabatte, die für jede Preisgruppe verknüpft sind.

## <a name="example-channel-discount-set-up"></a>Beispieleinrichtung für Kanalrabatte
Das folgende Beispiel veranschaulicht die Aufgaben zur Einrichtung von Kanalrabatten.

1.  In vorliegenden Beispiel haben Sie einen Kanal namens **Houston** und erstellen einen neuen Rabatt namens **Zurück zur Schule.**
2.  Da die Preisgestaltungs- und Rabattstrategie die Möglichkeit von Kanalrabatten umfasst, erstellen Sie immer eine kanalspezifische Preisgruppe, wenn Sie einen Kanal erstellen.
3.  Sie haben die Preisgruppe **Houston-PG** und diese ist dem Kanal **Houston** zugewiesen.
4.  Nachdem Sie den neuen Rabatt **Zurück zur Schule** erstellt haben, müssen Sie auf **Preisgruppen** oben auf der Seite **Rabatt** klicken. Die **Rabattpreisgruppen**-Seite wird geöffnet. Danach klicken Sie auf **Neu** und wählen die Preisgruppe **Houston-PG** aus.
5.  Jetzt können Sie den Rabatt aktivieren und für den Kanal umsetzen.

 

<a name="see-also"></a>Siehe auch
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


