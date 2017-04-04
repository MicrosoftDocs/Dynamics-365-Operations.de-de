---
title: "Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch"
description: In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist obligatorisch.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch

In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist obligatorisch.

Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.
-   Die Lagerortdimension ist als obligatorische Dimension festgelegt und muss zwingend für die Bedarfsbuchung angegeben werden.
-   Die Standort- und Lagerortdimension werden für die Disposition festgelegt. Für die Disposition können auch andere Dimensionen festgelegt werden. Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.

In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht. Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:
-   The warehouse is set to **Manual**. ** Auf Lagerverwaltungs-Einstellungs-Bestandsaufschlüsselung &gt; Lagerorte &gt; **. Wählen Sie auf dem Inforegister **Produktprogrammplanung** das Feld **Manuell**.
-   Für den Artikel ist die Artikeldeckung definiert. ** Produktinformationsverwaltung auf Produkt-freigegebeneProdukte &gt; **&gt;. Wählen Sie den Artikel aus, und klicken Sie dann im Aktivitätsbereich, auf der Registerkarte, Plan ** ** auf aus ** Artikeldeckung **.
-   Für den Lagerort sind Auffüllbeziehungen definiert. ** Auf Lagerverwaltungs-Einstellungs-Bestandsaufschlüsselung &gt; Lagerorte &gt; **. Wählen Sie auf dem Inforegister **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.
-   Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt. ** Produktinformationsverwaltung auf Produkt-freigegebeneProdukte &gt; **&gt;. Wählen Sie den Artikel aus, und klicken Sie dann im Aktivitätsbereich, auf der Registerkarte, Plan ** ** auf aus ** Standardauftragseinstellungen **. Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.

![Disposition an Bedarfsstandort und Lagerort, Lagerort obligatorisch](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Siehe auch
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch](master-plan-site-coverage-warehouse-not-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Produktprogrammplanungslauf - Ermittlung der Stücklistenversion](master-plan-bom-version-determined.md)


