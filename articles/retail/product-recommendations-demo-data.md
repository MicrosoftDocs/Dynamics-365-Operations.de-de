---
title: Omni-Channel-Produkt-Empfehlungsdemodaten
description: Dieses Dokument bietet Richtlinien zur Nutzung von Omni-Channel-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225955"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Omni-Channel-Produkt-Empfehlungsdemodaten

Dieses Dokument bietet Richtlinien zur Nutzung von Omni-Channel-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.

Omni-Channel-Produktempfehlungen bieten einen Satz redaktionell zusammengestellter oder programmgesteuert generierter geordneter Liste von Produkten. Diese Liste kann in einigen Szenarien je nach Geschäftsanforderung verwendet werden. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendaitons-overview.md).

Für Stufe 2 und höhere Dynamics-Umgebungen werden Produktempfehlungen automatisch basierend auf Kundendaten berechnet.
Das Verwenden der Empfehlungsdemodaten deaktiviert keine Produktempfehlungslösung, die bereits in der Umgebung ist und keine der seiner Nutzung zugeordneten Kosten.

Bei Umgebungen der Stufe 1 basieren Produktempfehlungen nur auf den statischen Demodaten, die in einer csv-Datei gespeichert werden.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivieren von Produktempfehlungsdemodaten in einer Umgebung

Debitoren müssen die **Dynamics 365 Commerce-Vorschaudemoerweiterung** in der entsprechenden Umgebung bereitstellen, die automatisch Produktempfehlungsdemodaten aktiviert.

## <a name="default-demo-data"></a>Standarddemodaten
Jede Einzelfeld-Typumgebung verfügt über einen Satz vorab installierter Produktempfehlungsdemodaten, die in der Koma getrennten Datei **„reco_demo_data.csv“** im gleichen Ordner wie das Dokument auf Retail Server gespeichert ist.

Diese Daten werden in den folgenden Spalten strukturiert

| Spaltenname         | Obligatorisch          | Beschreibung                                                                                                                                 | Mögliche Werte                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Der bestimmte Produktempfehlungslistentyp, den der Demodatpunkt generieren soll.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Die bestimmte Organisationseinheitsnummer, in der Produktempfehlungen auftauchen sollen.                                        |                                                                              |
| Kategorie            |                    |    Die Kategorie, für die die bestimmte Liste zurückgegeben werden soll. Wenn keine Kategorie angegeben wird, gilt die Liste nur für den Anfang der Navigationshierarchie.    |                                                                              |
| SeedItemId          |                    |    Für Listen, für die ein Seed (RecoPeopleAlsoBuy und RecoCart) erforderlich ist, ist es das Produkt, für das diese Listen weitere Produkte anzeigen sollten.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Mindestens ein Produkt, das als Ergebnis durch **„;“** getrennt zurückgegeben wird.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Demodaten anpassen
Debitoren können die Standarddemodaten mit sämtlichen Produkt und Kategorieinformationen bearbeiten, die in der Hauptniederlassung konfiguriert werden. Sobald die CSV aktualisiert wird, werden die Produktempfehlungen, die den Kunden zurückgesendet werden, diese Änderungen wiedergeben.

Die Erweiterung enthält die Datendatei RecoMockDataset.csv, mit der ein Debitor den Datensatz für die Scheinempfehlungsergebnisse steuern kann. Der Dateiname kann über die Erweiterungskonfiguration mithilfe der Einstellung **ext.Recommendations.DemoFilePath** gesteuert werden. Damit können die Kunden über mehrere Datasets verfügen, zwischen denen durch Konfiguration leicht gewechselt werden kann.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Produktempfehlungsübersicht](product-recommendations-overview.md)

[Umgebungsplanung](environment-planning.md)
