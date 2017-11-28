---
title: Interessent zu Bargeld
description: "Das Thema bietet eine Übersicht der Lösung „Interessent zu Bargeld” zwischen Dynamics 365 for Finance and Operations, Enterprise Edition, und Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>Interessent zu Bargeld  

[!include[banner](../includes/banner.md)]

Die Lösung „Interessent zu Bargeld” verwendet [Datenintegration](/common-data-service/entity-reference/dynamics-365-integration), um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, und Dynamics 365 for Sales hinweg mit dem Common Data Service (CDC) zu synchronisieren. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Während die Daten zwischen Finance and Operations und Sales fließen, können Sie Vertriebs- und Marketingaktivitäten in Dynamics 365 for Sales ausführen und die Auftagserfüllung mit Bestandsverwaltung in Finance and Operations handhaben. 

Diese Lösung bietet Integration in den folgenden Bereichen: 

-   [Konten in Sales verwalten und mit Finance and Operations synchronisieren](accounts-template-mapping.md)
-   [Kontakte in Sales verwalten und mit Finance and Operations synchronisieren](contacts-template-mapping.md)
-   [Produkte in Finance and Operations verwalten und mit Sales synchronisieren](products-template-mapping.md)
-   [Verkaufsangebote in Sales erstellen und mit Finance and Operations synchronisieren](sales-quotation-template-mapping.md)
-   [Verkaufsaufträge in Finance and Operations erstellen und mit Sales synchronisieren](sales-order-template-mapping.md)
-   [Verkaufsrechnungen in Finance and Operations erstellen und mit Sales synchronisieren](sales-invoice-template-mapping.md)

Diese Lösung bietet direkte Synchronisation in den folgenden Bereichen:

-   [Konten in Sales verwalten und direkt cvon Sales zu Finance and Operations synchronisieren](accounts-template-mapping-direct.md)
-   [Produkte in Finance and Operations verwalten und direkt mit Sales synchronisieren](products-template-mapping-direct.md)
-   [Kontakte in Sales verwalten und direkt mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)
-   [Angebotskopfzeilen und -positionen direkt von Sales zu Finance and Operations synchronisieren](sales-quotation-template-mapping-sales-fin.md)
-   [Verkaufsaufträge in Finance and Operations erstellen und direkt mit Sales synchronisieren](sales-order-template-mapping-direct.md)
-  [Auftragskopfzeilen und -positionen direkt zwischen Sales und Finance and Operations synchronisieren](sales-order-template-mapping-between-sales-fin.md)
-   [Synchronisieren von Aufträgen direkt zwischen Sales und Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
-   [Verkaufsrechnungen in Finance and Operations erstellen und direkt mit Sales synchronisieren](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Systemanforderungen für Dynamics 365 for Finance and Operations, Enterprise Edition

Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) mit Plattform-Update 8 (App 7.2.11792.56024 w/ Plattform 7.0.4565.16212)

- Hotfixes für Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017).
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - Dieser aktiviert Hotfix Unterstützung für Auftragssynchronisierung mit der Daten-Integrationsfunktion von Sales zu Finance and Operations, zusammen mit verschiedenen anderen Erweiterungen.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Dieser Hotfix aktiviert die Auftragspositionssynchronisierung mit der Datenintegrationsfunktion zwischen Finance and Operations und Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Dieser Hotfix aktiviert die Auftragspositionssynchronisierung mit der Datenintegrationsfunktion zwischen Finance and Operations und Sales.

**Hinweis**: Sie müssen nur KB4045570 installieren, da diese Installation Änderungen aus den anderen KB's enthält.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Systemanforderungen für Dynamics 365 for Sales

Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:

- Dynamics 365 for Sales, Version 1612 (8.2.1.207) (DB 8.2.1.207) online.
- Interessent zu Bargeld-Lösung für Dynamics 365 for Sales, Version 1.14.0.0 (v14) oder höher.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installieren der Interessent zu Bargeld-Lösung für Sales

- Laden Sie die [Interessent zu Bargeld-Lösungspaket-ZIP-Datei für Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) von CustomerSource herunter.

- Stellen Sie sicher, dass die ZIP-Datei nicht gesperrt ist, damit Sie beim Installieren des Lösungspakets keine Fehlermeldung erhalten, die besagt, dass keine Importpakete gefunden wurden. Führen Sie die folgenden Schritte aus, um die Datei zu entsperren:

    -  Klicken Sie mit der rechten Maustaste auf die ZIP-Datei.
    -  Wählen Sie **Eigenschaften** und **Entsperren** aus. 

- Entpacken Sie die Datei, und führen Sie PackageDeployer.exe aus.

- Installieren Sie die Interessent zu Bargeld-Cash-Lösung auf Ihrer Sales-Instance.

    - Wählen Sie den **Office 365**-Bereitstellungstyp aus.
    - Wählen Sie die Option zum **Anzeigen von Erweiterungen** aus.
    - Wählen Sie für eine schnelle Installation **Region** aus. Wenn Sie **Ich weiß nicht** auswählen, sucht das System nach allen Regionen und die Installation dauert länger.
    - Geben Sie **Benutzername** und **Kennwort** für einen Administratorbenutzer ein, der über Benutzerrechte zum Installieren verfügt.

