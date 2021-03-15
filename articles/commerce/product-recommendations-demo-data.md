---
title: Erstellen Sie Empfehlungen mit Demo-Daten
description: Dieses Thema bietet Richtlinien zur Nutzung von Mehrkanal-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ccb0b6c5aace0fc76c6886299fba7369abed860
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972364"
---
# <a name="create-recommendations-with-demo-data"></a>Erstellen Sie Empfehlungen mit Demo-Daten

[!include [banner](includes/banner.md)]

Dieses Thema bietet Richtlinien zur Nutzung von Mehrkanal-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.

Mehrkanal-Produktempfehlungen bieten eine Reihe von redaktionell kuratierten oder programmatisch erstellten Produktlisten. Diese Liste kann in einigen Szenarien je nach Geschäftsanforderung verwendet werden. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).

Für Stufe 2 und höhere Dynamics 365-Umgebungen werden Produktempfehlungen automatisch basierend auf Kundendaten berechnet. Das Verwenden der Empfehlungsdemodaten deaktiviert keine Produktempfehlungslösung, die bereits in der Umgebung ist und keine der seiner Nutzung zugeordneten Kosten.

Bei Umgebungen der Stufe 1 basieren Produktempfehlungen nur auf den statischen Demodaten, die in einer .csv-Datei gespeichert werden.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivieren von Produktempfehlungsdemodaten in einer Umgebung
Um Demo-Daten für Produktempfehlungen zu aktivieren, müssen Sie die Dynamics 365 Commerce-Vorschau-Demoerweiterung für die entsprechende Umgebung bereitstellen. Wenn Sie dies automatisch tun, werden Demo-Daten für Produktempfehlungen aktiviert.

## <a name="default-demo-data"></a>Standarddemodaten
Jede OneBox-Typumgebung verfügt über einen Satz vorab installierter Produktempfehlungsdemodaten, die in der Komma getrennten Datei „reco_demo_data.csv“ in der Commerce Scale Unit gespeichert ist.

Die Daten werden in den folgenden Spalten strukturiert.

| Spaltenname         | Obligatorisch          | Beschreibung                                                                                                                                 | Mögliche Werte                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Der bestimmte Produktempfehlungslistentyp, den der Demodatenpunkt generieren soll.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Die bestimmte Organisationseinheitsnummer, in der Produktempfehlungen angezeigt werden sollen.                                        |                                                                              |
| Kategorie            |                    |    Die Kategorie, für die die bestimmte Liste zurückgegeben werden soll. Wenn keine Kategorie angegeben wird, gilt die Liste nur für den Anfang der Navigationshierarchie.    |                                                                              |
| SeedItemId          |                    |    Für Listen, für die ein Seed (RecoPeopleAlsoBuy und RecoCart) erforderlich ist, ist es das Produkt, für das diese Listen weitere Produkte anzeigen sollten.            |                                                                              |
| CustomerId          |                    |    Für Listen, für die eine Kundenkennung erforderlich ist (RecoPicks).  Der Standardwert '0' gilt für alle Kunden.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Mindestens ein Produkt, das als Ergebnis durch ';'getrennt zurückgegeben wird.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Demodaten anpassen
Sie können die Standarddemodaten mit sämtlichen Produkt und Kategorieinformationen bearbeiten, die in der Hauptniederlassung konfiguriert werden. Nachdem Sie die .csv aktualisiert haben, werden die Produktempfehlungen, die den Kunden zurückgesendet werden, diese Änderungen wiedergeben.

Die Erweiterung enthält die Datendatei „RecoMockDataset.csv“, mit der Sie den Datensatz für die Scheinempfehlungsergebnisse steuern können. Der Dateiname kann über die Erweiterungskonfiguration mithilfe der Einstellung **ext.Recommendations.DemoFilePath** gesteuert werden. Damit können Sie über mehrere Datasets verfügen, zwischen denen durch Konfiguration leicht gewechselt werden kann.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]