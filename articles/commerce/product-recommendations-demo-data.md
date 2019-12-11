---
title: Abrufen von Produktempfehlungen mithilfe von Demodaten
description: Dieses Dokument bietet Richtlinien zur Nutzung von Mehrkanal-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697933"
---
# <a name="get-product-recommendations-using-demo-data"></a>Abrufen von Produktempfehlungen mithilfe von Demodaten
Dieses Dokument bietet Richtlinien zur Nutzung von Mehrkanal-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.

Mehrkanal-Produktempfehlungen bieten eine Reihe von redaktionell kuratierten oder programmatisch erstellten Produktlisten. Diese Liste kann in einigen Szenarien je nach Geschäftsanforderung verwendet werden. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).

Für Stufe 2 und höhere Dynamics 365-Umgebungen werden Produktempfehlungen automatisch basierend auf Kundendaten berechnet. Das Verwenden der Empfehlungsdemodaten deaktiviert keine Produktempfehlungslösung, die bereits in der Umgebung ist und keine der seiner Nutzung zugeordneten Kosten.

Bei Umgebungen der Stufe 1 basieren Produktempfehlungen nur auf den statischen Demodaten, die in einer .csv-Datei gespeichert werden.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivieren von Produktempfehlungsdemodaten in einer Umgebung
Um Demo-Daten für Produktempfehlungen zu aktivieren, müssen Sie die Dynamics 365 Commerce-Vorschau-Demoerweiterung für die entsprechende Umgebung bereitstellen. Wenn Sie dies automatisch tun, werden Demo-Daten für Produktempfehlungen aktiviert.

## <a name="default-demo-data"></a>Standarddemodaten
Jede Einzelfeld-Typumgebung verfügt über einen Satz vorab installierter Produktempfehlungsdemodaten, die in der Koma getrennten Datei „reco_demo_data.csv“ auf Retail Server gespeichert ist.

Die Daten werden in den folgenden Spalten strukturiert.

| Spaltenname         | Obligatorisch          | Beschreibung                                                                                                                                 | Mögliche Werte                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Der bestimmte Produktempfehlungslistentyp, den der Demodatenpunkt generieren soll.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Die bestimmte Organisationseinheitsnummer, in der Produktempfehlungen angezeigt werden sollen.                                        |                                                                              |
| Kategorie            |                    |    Die Kategorie, für die die bestimmte Liste zurückgegeben werden soll. Wenn keine Kategorie angegeben wird, gilt die Liste nur für den Anfang der Navigationshierarchie.    |                                                                              |
| SeedItemId          |                    |    Für Listen, für die ein Seed (RecoPeopleAlsoBuy und RecoCart) erforderlich ist, ist es das Produkt, für das diese Listen weitere Produkte anzeigen sollten.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Mindestens ein Produkt, das als Ergebnis durch „;“ getrennt zurückgegeben wird.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Demodaten anpassen
Sie können die Standarddemodaten mit sämtlichen Produkt und Kategorieinformationen bearbeiten, die in der Hauptniederlassung konfiguriert werden. Sobald Sie die .csv aktualisiert haben, werden die Produktempfehlungen, die den Kunden zurückgesendet werden, diese Änderungen wiedergeben.

Die Erweiterung enthält die Datendatei „RecoMockDataset.csv“, mit der Sie den Datensatz für die Scheinempfehlungsergebnisse steuern können. Der Dateiname kann über die Erweiterungskonfiguration mithilfe der Einstellung **ext.Recommendations.DemoFilePath** gesteuert werden. Damit können Sie über mehrere Datasets verfügen, zwischen denen durch Konfiguration leicht gewechselt werden kann.


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Umgebungsplanung](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)