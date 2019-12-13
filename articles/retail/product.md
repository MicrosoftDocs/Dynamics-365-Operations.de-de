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
ms.openlocfilehash: 98c84e987c40adf136d0240117f7b0f119bf2f59
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811116"
---
# <a name="product-recommendations-on-pos"></a>Produktempfehlungen zu POS

[!include [banner](includes/banner.md)]

Im Kern sind Produktempfehlungen eine formende Geschäftsanwendung, die alle Einzelhandelsplätze abdecken, um eine reichhaltige, ansprechende und angepasste Produkterfassungserfahrungen zu ermöglichen. Um diese Funktion in POS zu implementieren, führen Sie die Schritte zu [Empfehlungen Ihren POS-Geräten hinzufügen](add-recommendations-control-pos-screen.md) aus. 

Weitere Informationen zu Produktempfehlungsfunktionen finden Sie im [Produktempfehlungsüberblick](../commerce/product-recommendations.md). 

## <a name="scenarios"></a>Szenarien

Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert. Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.

1. Auf der **Produktdetails** Seite:

    - Wenn ein Filialmitarbeiter eine **Produktdetails** Seite besucht, wenn er frühere Transaktionen über verschiedene Kanäle betrachtet, schlägt der Empfehlungsdienst zusätzliche Artikel vor, die wahrscheinlich zusammen gekauft werden.

    [![Empfehlungen zur Produktdetailseite](./media/proddetails.png)](./media/proddetails.png)

2. Auf der **Transaktionen** Seite:

    - Die Empfehlungs-Engine schlägt Artikel vor, die auf der gesamten Liste der Artikel im Warenkorb basieren, die häufig zusammen gekauft werden.

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
- Wenn Sie weitere Fragen haben, lesen Sie die [Produktempfehlungen FAQ](../commerce/faq-recommendations.md) für weitere Informationen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Ein Empfehlungssteuerelement des Transaktionsbildschirms auf POS-Geräten](add-recommendations-control-pos-screen.md)

[Überblick über Produktempfehlungen](../commerce/product-recommendations.md)

[Produktempfehlungen aktivieren](../commerce/enable-product-recommendations.md) 
