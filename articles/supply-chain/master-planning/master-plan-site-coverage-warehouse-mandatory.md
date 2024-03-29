---
title: Hauptplanung für Standortdeckung, Lagerort obligatorisch
description: In diesem Artikel wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist eine zwingende Dimension.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df58017c25737cc946d09bf86ff7ad8bd33f4176
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741039"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Hauptplanung für Standortdeckung, Lagerort obligatorisch

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist eine zwingende Dimension.

Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden. Diese Einstellung kann nicht geändert werden.
-   Die Lagerortdimension ist als obligatorische Dimension festgelegt und muss zwingend für die Bedarfsbuchung angegeben werden.
-   Die Standortdimension ist für die Disposition festgelegt. Für die Disposition können auch andere Dimensionen festgelegt werden. Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.
-   Die Lagerortdimension ist nicht für die Disposition festgelegt. Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.

In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht. Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:
-   Für den Artikel ist die Artikeldeckung definiert. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.
-   Für den Lagerort sind Auffüllbeziehungen definiert. Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**. Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.
-   Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**. Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.

![Bedarf für Disposition an Standort, Lagerort obligatorisch.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Übersicht über Produktprogrammpläne und Funktionen für mehrere Standorte](master-plan-multisite-functionality.md)
- [Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Hauptplanung für Standortdeckung, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)
- [Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Die Stücklistenversion bestimmen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]