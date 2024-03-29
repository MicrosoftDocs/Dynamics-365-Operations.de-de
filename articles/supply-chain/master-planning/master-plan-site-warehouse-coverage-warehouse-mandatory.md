---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch
description: In diesem Artikel wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist obligatorisch.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcb2d41ff70714b6bc9c28f3e23ce95f5292f2e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740058"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist obligatorisch.

Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.
-   Die Lagerortdimension ist als obligatorische Dimension festgelegt und muss zwingend für die Bedarfsbuchung angegeben werden.
-   Die Standort- und Lagerortdimension werden für die Disposition festgelegt. Für die Disposition können auch andere Dimensionen festgelegt werden. Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.

In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht. Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:
-   Der Lagerort ist auf **Manuell** festgelegt. Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**. Wählen Sie auf dem Inforegister **Produktprogrammplanung** das Feld **Manuell**.
-   Für den Artikel ist die Artikeldeckung definiert. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Artikeldeckung**.
-   Für den Lagerort sind Auffüllbeziehungen definiert. Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**. Wählen Sie auf dem Inforegister **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.
-   Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Standardauftragseinstellungen**. Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.

![Disposition an Bedarfsstandort und Lagerort, Lagerort obligatorisch.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Übersicht über Produktprogrammpläne und Funktionen für mehrere Standorte](master-plan-multisite-functionality.md)
- [Hauptplanung für Standortdeckung, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)
- [Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Die Stücklistenversion bestimmen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]