---
title: Produktempfehlungen zu POS
description: In diesem Thema wird die Verwendung der Produktempfehlungen bei einem Verkaufsstelle (POS)-Gerät beschrieben.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278378"
---
# <a name="product-recommendations-on-pos"></a>Produktempfehlungen zu POS

[!include [banner](includes/banner.md)]

Im Kern sind Produktempfehlungen eine formende Geschäftsanwendung, die alle Einzelhandelsplätze abdecken, um eine reichhaltige, ansprechende und angepasste Produkterfassungserfahrungen zu ermöglichen. Um diese Funktion in POS zu implementieren, führen Sie die Schritte zu [Empfehlungen Ihren POS-Geräten hinzufügen](add-recommendations-control-pos-screen.md) aus. 

Weitere Informationen zu Produktempfehlungsfunktionen finden Sie im [Produktempfehlungsüberblick](../commerce/product-recommendations.md). 

## <a name="scenarios"></a>Szenarien

Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert. Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.

1. Auf der **Produktdetails** Seite:

    - • Wenn ein Shopmitarbeiter eine **Produktdetails**-Seite besucht, wenn er auf die vorherigen Buchungen über verschiedene Kanäle schaut, schlägt der Empfehlungsdienst zusätzliche Artikel vor, die wahrscheinlich zusammen eingekauft werden.

    [![Empfehlungen zur Produktdetailseite](./media/proddetails.png)](./media/proddetails.png)

2. Auf der **Transaktionen** Seite:

    - • Das Empfehlungsmodul schlägt Artikel auf Basis der gesamten Artikelliste im Korb vor, die häufig zusammen eingekauft werden.

    > [!NOTE]
    > Zum Anzeigen von Empfehlungen auf der Seite **Buchung** muss der Einzelhändler das Bildschirmlayout in Dynamics 365 for Retail aktualisieren. Das Steuerelement **Empfehlungen** muss auf der Seite **Buchung** abgelegt werden.

    [![Empfehlungen auf de Seite „Transaktion“](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>Konfigurieren Sie Dynamics 365 Retail, um POS-Empfehlungen zu aktivieren

Gehen Sie zum Einrichten von Produktempfehlungen folgendermaßen vor:

1. Stellen Sie sicher, dass Ihr Service auf **10.0.6 Build** aktualisiert wurde.
2. Befolgen Sie die Anweisungen zur Vorgehensweise für das [Aktivieren von Produktempfehlungen](../commerce/enable-product-recommendations.md) für Ihr Unternehmen.
3. Optional: Um Empfehlungen zum Buchungsbildschirm anzuzeigen, navigieren Sie zu **Bildschirmlayout**, wählen das Bildschirmlayout, starten den **Bildschirmlayoutdesigner** und dann legen das **Empfehlungssteuerelement** ab.
4. Wechseln Sie **Einzelhandelsparameter**, wählen Sie **Machine-Llearning** aus, wählen Sie die Option **Ja** unter **POS-Empfehlungen aktivieren** aus.
5. Weitere Empfehlungen zu POS erhalten Sie mit dem Konfigurationseinzelvorgang **1110**. Um Änderungen widerzuspiegeln der im POS-Designer durchgeführt wurden, aktivieren Sie Kanalkonfigurationseinzelvorgang **1070**.



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Beheben Sie Probleme, wo Sie Produktempfehlungen bereits aktiviert haben

- Navigieren Sie zu **Retail-Parameter** \> **Empfehlungslisten** \> **Produktempfehlungen deaktivieren** und **globalen Konfigurationsauftrag \[9999\]** ausführen. 
- Wenn Sie die **Empfehlungssteuerung** Ihrem Buchungsbildschirm mithilfe von **Designer für Bildschirmlayout** hinzugefügt haben, entfernen Sie diese auch.
- Wenn zusätzliche Fragen haben, sehen Sie sich unsere [Häufig gestellten Fragen zu Empfehlungen](../commerce/faq-recommendations.md) an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Empfehlungssteuerelements zu einer Buchungsseite auf einem POS-Gerät](add-recommendations-control-pos-screen.md)
[Produktempfehlungsüberblick](../commerce/product-recommendations.md)
[Aktivieren von Produktempfehlungen](../commerce/enable-product-recommendations.md) 
