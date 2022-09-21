---
title: Produktempfehlungen im POS hinzufügen
description: In diesem Artikel wird die Verwendung der Produktempfehlungen bei einem Verkaufsstelle (POS)-Gerät beschrieben.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460055"
---
# <a name="add-product-recommendations-on-pos"></a>Produktempfehlungen im POS hinzufügen

[!include [banner](includes/banner.md)]

Im Kern handelt es sich bei den Produktempfehlungen um eine transformative Geschäftsanwendung, die sich über alle Handelsbereiche erstreckt, um reichhaltige, ansprechende und maßgeschneiderte Erfahrungen bei der Produktfindung zu schaffen. Um diese Funktion in POS zu implementieren, führen Sie die Schritte zu [Empfehlungen Ihren POS-Geräten hinzufügen](add-recommendations-control-pos-screen.md) aus. 

Weitere Informationen zu Produktempfehlungsfunktionen finden Sie im [Produktempfehlungsüberblick](../commerce/product-recommendations.md). 

## <a name="scenarios"></a>Szenarien

Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert. Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.

1. Auf der **Produktdetails** Seite:

    - Wenn ein Filialmitarbeiter eine **Produktdetails** Seite besucht, wenn er frühere Transaktionen über verschiedene Kanäle betrachtet, schlägt der Empfehlungsdienst zusätzliche Artikel vor, die wahrscheinlich zusammen gekauft werden. Abhängig von den Add-Ons für den Service können Einzelhändler **Ähnliche Outfits kaufen**- und **Ähnliche Beschreibung einkaufen**-Empfehlungen für Produkte anzeigen, zusätzlich zu personalisierten Empfehlungen für Benutzer, die eine vorherige Kaufhistorie haben.

    [![Empfehlungen zur Produktdetailseite.](./media/proddetails.png)](./media/proddetails.png)

2. Auf der **Transaktionen** Seite:

    - Die Empfehlungs-Engine schlägt Artikel vor, die auf der gesamten Liste der Artikel im Warenkorb basieren, die häufig zusammen gekauft werden.

    > [!NOTE]
    > Zum Anzeigen von Empfehlungen auf der Seite **Buchung** muss der Einzelhändler das Bildschirmlayout in Dynamics 365 Commerce aktualisieren. Das Steuerelement **Empfehlungen** muss auf der Seite **Buchung** abgelegt werden.

    [![Empfehlungen auf der Seite „Transaktion“.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigurieren Sie Commerce, um POS-Empfehlungen zu aktivieren 

Bestätigen Sie zum Einrichten von Produktempfehlungen, dass Sie den Bereitstellungsprozess für E-Commerce-Produktempfehlungen abgeschlossen haben, indem Sie die Schritte in [Produktempfehlungen aktivieren](../commerce/enable-product-recommendations.md) ausführen. Standardmäßig werden Empfehlungen auf der **Produktdetails**-Seite und der **Kundendetails**-Seite angezeigt, nachdem Sie die Bereitstellungsschritte abgeschlossen haben und die Daten erfolgreich gekocht wurden. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Empfehlungen dem Transaktionsbildschirm hinzufügen

1. Um Empfehlungen zum Transaktionsbildschirm hinzuzufügen, folgen Sie den Schritten in [Fügen Sie dem Transaktionsbildschirm Empfehlungen hinzu](add-recommendations-control-pos-screen.md).
1. Führen Sie den Kanalkonfigurationsjob **1070** in Commerce headquarters aus, um Änderungen wiederzugeben, die im POS-Bildschirmlayout-Designer vorgenommen wurden.

> [!NOTE] 
> Wenn Sie POS-Empfehlungen mithilfe der CSV-Datei (Comma-Separated Values) von RecoMock aktivieren möchten, müssen Sie die CSV-Datei in der Microsoft Dynamics Lifecycle Services (LCS)-Objektbibliothek, bevor Sie den Layout-Manager konfigurieren. Wenn Sie die RecoMock-CSV-Datei verwenden, müssen Sie keine Empfehlungen aktivieren. Die CSV-Datei steht nur zu Demozwecken zur Verfügung. Es wird für Kunden oder Lösungsarchitekten empfohlen, die das Erscheinungsbild von Empfehlungslisten zu Demozwecken nachahmen möchten, ohne eine zusätzliche Lagerhaltungseinheit (SKU) kaufen zu müssen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
