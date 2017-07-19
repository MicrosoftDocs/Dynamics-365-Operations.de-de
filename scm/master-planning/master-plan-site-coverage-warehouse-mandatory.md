---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch
description: In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist eine zwingende Dimension.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a1bf8f2253c63e4b6ca8fee02ec6b1cfb8aad73c
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist eine zwingende Dimension.

Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden. Diese Einstellung kann nicht geändert werden.
-   Die Lagerortdimension ist als obligatorische Dimension festgelegt und muss zwingend für die Bedarfsbuchung angegeben werden.
-   Die Standortdimension ist für die Disposition festgelegt. Für die Disposition können auch andere Dimensionen festgelegt werden. Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.
-   Die Lagerortdimension ist nicht für die Disposition festgelegt. Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.

In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht. Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:
-   Für den Artikel ist die Artikeldeckung definiert. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.
-   Für den Lagerort sind Auffüllbeziehungen definiert. Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**. Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.
-   Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**. Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.

![Bedarf für Disposition an Standort, Lagerort obligatorisch](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Siehe auch
--------

[Produktprogrammplanung und Funktion für mehrere Standorte](master-plan-multisite-functionality.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Produktprogrammplanungslauf - Ermittlung der Stücklistenversion](master-plan-bom-version-determined.md)




