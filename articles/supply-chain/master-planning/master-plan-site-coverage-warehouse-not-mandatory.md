---
title: Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch
description: In diesem Artikel wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03bd1970aa7a2f3276186a0a9f8c2cd2880956
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741148"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird.

Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.
-   Die Lagerortdimension ist nicht auf obligatorisch festgelegt. Der Lagerort ist unter Umständen bekannt, wird jedoch nicht in der Produktprogrammplanberechnung verwendet.
-   Die Standortdimension ist für die Disposition festgelegt.
-   Die Lagerortdimension ist nicht für die Disposition festgelegt. Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.

In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht. Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:
-   Für den Artikel ist die Artikeldeckung definiert. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.
-   Für den Lagerort sind Auffüllbeziehungen definiert. Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**. Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.
-   Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**. Im Formular **Standardauftragseinstellungen** sehen Sie das Feld **Standardauftragstyp**.

![Bedarf für Disposition an Standort, Lagerort nicht obligatorisch.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Übersicht über Produktprogrammpläne und Funktionen für mehrere Standorte](master-plan-multisite-functionality.md)
- [Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)
- [Hauptplanung für Standortdeckung, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Die Stücklistenversion bestimmen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]